---
title: What is the method to obtain the "id" following the insertion of data into a MySQL database using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `lastrowid` attribute of the database cursor object to retrieve the id of the last inserted row.
---

**Contents**

[TOC]

**Section 1: Introduction**

When inserting data into a MySQL database with Python, it is often necessary to retrieve the `id` of the newly created record. This `id` can be useful for referencing the record in future queries and operations. 

In this guide, we will explore several methods for retrieving the `id` after an INSERT operation in Python.

**Section 2: Retrieving the last inserted id with MySQL**

MySQL provides a built-in function for retrieving the `id` of the last inserted record. We can use this function with Python to retrieve the `id` after an INSERT operation. 

Assuming we have a MySQL connection object named `conn` and a cursor object named `cursor`, the following code can be used to retrieve the last inserted `id`:

```python
cursor.execute("INSERT INTO my_table (column1, column2) VALUES (%s, %s)", (value1, value2))
last_id = cursor.lastrowid
```

Here, `my_table` is the name of the table we are inserting data into, and `column1` and `column2` are the names of the columns we are inserting values into. `value1` and `value2` are Python variables containing the values we want to insert.

The `execute()` method is used to execute the INSERT statement, and the `lastrowid` property of the cursor object is used to retrieve the `id` of the last inserted record.

**Section 3: Retrieving the last inserted id with SQLAlchemy**

If you are using the SQLAlchemy library to interact with a MySQL database in Python, you can also retrieve the last inserted `id` using the `inserted_primary_key` property of the `ResultProxy` object.

Assuming we have a SQLAlchemy `engine` object and a `Session` object, the following code can be used to retrieve the last inserted `id`:

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import Session

engine = create_engine('mysql+pymysql://user:password@host/database_name')
session = Session(engine)

new_object = MyTable(column1=value1, column2=value2)
session.add(new_object)
session.commit()

last_id = session.execute('SELECT LAST_INSERT_ID()').fetchone()[0]
```

In this code, we first create an instance of the `MyTable` class with the values we want to insert. We then add the object to the `Session`, commit the transaction, and retrieve the last inserted `id` using a SELECT statement and the `LAST_INSERT_ID()` function.

**Section 4: Conclusion**

In this guide, we explored two methods for retrieving the `id` of a newly inserted record in a MySQL database in Python. Whether you are using the built-in MySQL function or the SQLAlchemy library, it is easy and efficient to retrieve the `id` of a newly inserted record in your Python code.
