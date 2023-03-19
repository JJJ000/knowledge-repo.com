---
title: Select where sqlalchemy is not null
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use `isnot(None)` in a filter statement for a SQLAlchemy query to select non-`NULL` values.
---

**Contents**

[TOC]

Section 1: Introduction
SQLAlchemy is a Python package that provides a way to work with databases in Python. It is a popular library used by developers to build and interact with databases. The library provides a large number of features and functionalities, including support for querying databases. In this tutorial, we will look at how to perform a SQLAlchemy IS NOT NULL select in Python.

Section 2: Setting up a Connection to a Database
Before we can perform any queries on a database, we need to establish a connection to the database. In SQLAlchemy, we can use the create_engine() function to create a connection to a database. The create_engine() function requires the connection string and any additional parameters we want to pass to the engine. Here is an example of how to create a connection to a MySQL database using SQLAlchemy:

```python
from sqlalchemy import create_engine

engine = create_engine("mysql+pymysql://username:password@localhost/mydatabase")
```

Section 3: Performing a SQLAlchemy IS NOT NULL SELECT
Once we have established a connection to the database, we can perform a SQLAlchemy IS NOT NULL select by using the select() function. The select() function allows us to query the database and return the data we are interested in. In addition to the columns we want to select, we can also specify any filtering or sorting criteria we want to use. Here is an example of how to perform a SQLAlchemy IS NOT NULL select in Python:

```python
from sqlalchemy import select
from sqlalchemy.orm import sessionmaker

Session = sessionmaker(bind=engine)
session = Session()

stmt = select(<table_name>).where(<column_name> is not None)
result = session.execute(stmt)

for row in result:
    print(row)
```

In this example, we first create a session using the Session() class of SQLAlchemy. Then, we use the select() function to construct a SELECT statement that selects all columns from a given table where a given column is not null. We then execute the SELECT statement using the session.execute() method, which returns a result set. Finally, we iterate over the result set and print each row.

Section 4: Conclusion
In this tutorial, we looked at how to perform a SQLAlchemy IS NOT NULL select in Python. We started by establishing a connection to a database using the create_engine() function. Then, we used the select() function to construct a SELECT statement that selects all columns from a given table where a given column is not null. Finally, we executed the SELECT statement using the session.execute() method and printed the result set. SQLAlchemy provides a rich and powerful set of APIs for working with databases, allowing developers to perform complex queries and manage their data efficiently.
