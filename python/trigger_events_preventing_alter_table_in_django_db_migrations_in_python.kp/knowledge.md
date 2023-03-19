---
title: The database migration of django cannot perform the alter table operation due to the presence of trigger events that are still pending
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You need to temporarily disable the triggers before executing the ALTER TABLE command in Django-DB-Migrations.
---

**Contents**

[TOC]

Possible answer:

# Issue description

When using Django-DB-Migrations to modify the schema of a database table, you may encounter an error message like this:

```
django.db.utils.OperationalError: cannot ALTER TABLE "my_table" because it has pending trigger events
```

This error occurs because there are triggers attached to the table that have not been executed yet, and modifying the table's structure may cause conflicts with those triggers. 

# Possible solutions

To solve this issue, you can try one or more of the following solutions:

## 1. Temporarily disable triggers

One way to avoid the conflict between triggers and schema changes is to disable the triggers before altering the table, and then re-enable them after the changes are done. You can do this manually in the database, or use a Django migration to automate the process.

Here's an example migration that disables and re-enables a trigger in PostgreSQL:

```python
from django.db import migrations, models

class Migration(migrations.Migration):

    dependencies = [
        ('my_app', '0001_initial'),
    ]

    operations = [
        migrations.RunSQL('ALTER TABLE my_table DISABLE TRIGGER my_trigger;'),
        migrations.AlterField(
            model_name='my_model',
            name='my_field',
            field=models.IntegerField(),
        ),
        migrations.RunSQL('ALTER TABLE my_table ENABLE TRIGGER my_trigger;'),
    ]
```

Note that this approach may not work for all types of triggers, depending on their implementation and purpose. Also, disabling triggers can have performance implications, especially if the table has a lot of data.

## 2. Wait for trigger events to complete

If you don't want to disable the triggers, you can wait for them to execute before modifying the table. This can be done by monitoring the system catalog tables for pending trigger events, and waiting for them to become zero.

Here's an example query that checks the number of pending triggers for a table in PostgreSQL:

```sql
SELECT tgname, tgrelid::regclass, tgenabled
FROM pg_trigger
WHERE tgrelid = 'public.my_table'::regclass
AND NOT tgenabled
AND tg_constraint = 0;
```

You can run this query periodically until it returns no rows, which means that all pending triggers have been executed. Then you can proceed with the schema changes.

Note that this approach can be time-consuming and may not be feasible if the table is constantly being updated or if the triggers take a long time to execute.

## 3. Modify triggers to accommodate schema changes

Another option is to modify the triggers themselves to accommodate the schema changes. For example, if you're adding a new column to a table, you can also modify the trigger function to update that column in the same transaction.

Here's an example trigger function that updates a new column "new_column" when a row is inserted:

```sql
CREATE OR REPLACE FUNCTION my_trigger_function()
RETURNS trigger AS
$$
BEGIN
   -- Update the old column as before
   NEW.old_column = OLD.old_column + 1;
   -- Update the new column with a default value
   NEW.new_column = 'default_value';
   RETURN NEW;
END;
$$ LANGUAGE plpgsql;
```

This way, the trigger can still be executed without conflict, and the new column gets populated as expected.

Note that this approach requires you to have control over the trigger function code, and may not be applicable for all scenarios. Additionally, modifying triggers may affect other parts of the system that rely on them, so you need to test and validate the changes carefully.

# Conclusion

When encountering the "cannot ALTER TABLE because it has pending trigger events" error in Django-DB-Migrations, you can try one or more of the solutions described above: disable triggers temporarily, wait for trigger events to complete, or modify triggers to accommodate schema changes. Each approach has its pros and cons, so choose the one that fits your specific case best.
