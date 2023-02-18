---
title: Change the name of an attribute in a postgresql jsonb field
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use ALTER TABLE to rename the jsonb field.
---

**Contents**

[TOC]

# Using ALTER TABLE

The ALTER TABLE statement can be used to rename an attribute in a jsonb field. This statement requires the table name, the name of the existing attribute, and the new name of the attribute. The syntax of the ALTER TABLE statement is as follows:

`ALTER TABLE <table_name> ALTER COLUMN <jsonb_field_name> RENAME ATTRIBUTE <existing_attribute_name> TO <new_attribute_name>;`

# Using UPDATE

The UPDATE statement can also be used to rename an attribute in a jsonb field. This statement requires the table name, the name of the existing attribute, and the new name of the attribute. The syntax of the UPDATE statement is as follows:

`UPDATE <table_name> SET <jsonb_field_name> = jsonb_set(<jsonb_field_name>, '{<new_attribute_name>}', <jsonb_field_name>->'<existing_attribute_name>') WHERE <jsonb_field_name>->'<existing_attribute_name>' IS NOT NULL;`

# Using PL/pgSQL

It is also possible to use a PL/pgSQL function to rename an attribute in a jsonb field. This requires the table name, the name of the existing attribute, and the new name of the attribute. The syntax of the PL/pgSQL function is as follows:

`CREATE OR REPLACE FUNCTION rename_jsonb_attribute(p_table_name TEXT, p_jsonb_field_name TEXT, p_existing_attribute_name TEXT, p_new_attribute_name TEXT)
RETURNS VOID AS
$$
BEGIN
    UPDATE p_table_name
    SET p_jsonb_field_name = jsonb_set(p_jsonb_field_name, '{<p_new_attribute_name>}', p_jsonb_field_name->'<p_existing_attribute_name>')
    WHERE p_jsonb_field_name->'<p_existing_attribute_name>' IS NOT NULL;
END;
$$
LANGUAGE plpgsql;`

# Using Python

The psycopg2 library can be used to rename an attribute in a jsonb field from within a Python script. This requires the table name, the name of the existing attribute, and the new name of the attribute. The syntax of the Python statement is as follows:

`import psycopg2
conn = psycopg2.connect(...)
cur = conn.cursor()
cur.execute("UPDATE <table_name> SET <jsonb_field_name> = jsonb_set(<jsonb_field_name>, '{<new_attribute_name>}', <jsonb_field_name>->'<existing_attribute_name>') WHERE <jsonb_field_name>->'<existing_attribute_name>' IS NOT NULL;")
conn.commit()`
