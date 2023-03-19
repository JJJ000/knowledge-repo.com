---
title: What is the procedure for performing inserts and updates in an upgrade script using alembic?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the SQLAlchemy API within the upgrade function to execute the desired inserts and updates.
---

**Contents**

[TOC]

# Introduction
Alembic is a tool used for database migrations in SQLAlchemy. It allows the user to write Python code that describes the changes to be made to the database schema. It can be used to execute inserts and updates in an Alembic upgrade script.

# Using SQLAlchemy ORM
One way to execute inserts and updates in Alembic upgrade script is by using SQLAlchemy ORM. In this approach, we first define the model classes for the tables we want to update or insert data into. Then, we create an instance of the session that connects to the database and use it to execute SQL statements.

```
from alembic import op
import sqlalchemy as sa
from sqlalchemy.orm import sessionmaker

Session = sessionmaker()

def upgrade():
    bind = op.get_bind()
    Session.configure(bind=bind)

    # Create a session and new object to insert into the database
    session = Session()
    new_obj = MyModelClass(foo='bar')
    session.add(new_obj)
    session.commit()

    # Update an existing object in the database
    obj_to_update = session.query(MyModelClass).filter(MyModelClass.id==1).first()
    obj_to_update.foo = 'baz'
    session.commit()


def downgrade():
    pass
```

# Using Raw SQL Queries
Another approach is to use raw SQL queries in the Alembic upgrade script. In this approach, we use the `op.get_bind()` method to get a connection to the database and execute the SQL queries.

```
from alembic import op

def upgrade():
    conn = op.get_bind()

    # Insert a new row into the table
    conn.execute("INSERT INTO my_table (foo, bar) VALUES ('baz', 1)")

    # Update an existing row in the table
    conn.execute("UPDATE my_table SET foo = 'qux' WHERE id = 1")


def downgrade():
    pass
```

# Conclusion
Both of these approaches can be used to execute inserts and updates in an Alembic upgrade script. The approach to use depends on the specific requirements of the task at hand. SQLAlchemy ORM provides a higher level of abstraction and can be easier to use, while raw SQL queries provide more control and flexibility.
