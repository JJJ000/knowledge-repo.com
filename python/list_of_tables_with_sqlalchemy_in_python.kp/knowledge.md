---
title: Obtaining a roster of tables using sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the `MetaData` object and its `tables` attribute to get a list of table objects.
---

**Contents**

[TOC]

Section 1: Introduction
SQLAlchemy is a popular Python library that provides a way to work with relational databases. One common task when working with databases is getting a list of tables from a database using Python code. In this tutorial, we will show you how to do this using SQLAlchemy.

Section 2: Setting up the Database Connection
The first thing we need to do is set up a connection to the database. We will assume that you have already installed SQLAlchemy and have a database set up. To establish a connection, we will use the create_engine function from the sqlalchemy module.

The create_engine function takes a database URL as an argument. The database URL specifies the type of database we are connecting to, as well as any additional parameters required to establish a connection. Here is an example of how to set up a connection to a SQLite database.

```python
from sqlalchemy import create_engine

engine = create_engine('sqlite:///example.db')
```

Section 3: Getting a List of Tables
To get a list of tables from the database, we can use the inspector object provided by SQLAlchemy. The inspector object allows us to inspect the metadata of a database and retrieve information such as the names and types of tables.

Here is an example of how to use the inspector object to get a list of tables from the SQLite database.

```python
from sqlalchemy import create_engine, inspect

engine = create_engine('sqlite:///example.db')

# Create an inspector object
inspector = inspect(engine)

# Get a list of table names
table_names = inspector.get_table_names()

print(table_names)
```

This code will output a list of table names in the example database.

Section 4: Conclusion
In this tutorial, we have shown you how to get a list of tables from a database using SQLAlchemy. We started by setting up a connection to the database using create_engine, and then used the inspector object to get a list of table names. This is a common task when working with databases, and knowing how to do it in SQLAlchemy can be very useful.
