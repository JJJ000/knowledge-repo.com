---
title: Using sqlalchemy orm for inserting multiple records at once
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `insert()` method of the ORM`s `session` object to perform bulk inserts in SQLAlchemy.
---

**Contents**

[TOC]

Section 1: Introduction to SQLAlchemy ORM 

SQLAlchemy is a Python library for working with databases. It provides an Object Relational Mapping (ORM), which allows us to map database tables to classes and objects in Python. This mapping makes it easy to work with databases in Python, without having to write raw SQL queries. SQLAlchemy ORM can be used with many different types of databases, including MySQL, SQLite, and PostgreSQL.

Section 2: Bulk Insert in SQLAlchemy ORM 

Bulk insert is a mechanism for inserting large amounts of data into a database in a single transaction. This can be much faster than inserting the data one row at a time, as each row requires a separate write operation. In SQLAlchemy ORM, bulk insert can be done using the insert() method of the Table object. This method takes a list of dictionaries as input, where each dictionary represents a row of data to be inserted into the table.

Section 3: Example of Bulk Insert with SQLAlchemy ORM 

Here is an example of how to do bulk insert with SQLAlchemy ORM:

```
from sqlalchemy import create_engine, Table, Column, Integer, String, MetaData

engine = create_engine("postgresql://user:password@host/database")
metadata = MetaData()

table = Table(
    "my_table",
    metadata,
    Column("id", Integer, primary_key=True),
    Column("name", String),
    Column("age", Integer),
)

data = [
    {"name": "John", "age": 20},
    {"name": "Jane", "age": 25},
    {"name": "Adam", "age": 30},
]

with engine.connect() as conn:
    conn.execute(table.insert().values(data))
```

In this example, we first create an engine object that connects to a PostgreSQL database. We then define the metadata for our table, and create a Table object that maps to our database table. We also define a list of dictionaries that represent the rows of data we want to insert.

Finally, we use the connect() method of the engine object to establish a connection to the database, and execute the insert() method of our table object to insert the data into the table in bulk.

Section 4: Conclusion 

Bulk insert is a powerful feature of SQLAlchemy ORM that can help us insert large amounts of data into a database quickly and efficiently. By using the insert() method with a list of dictionaries, we can insert multiple rows of data in a single transaction. This can save us time and improve the performance of our database operations.
