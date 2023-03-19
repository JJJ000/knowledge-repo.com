---
title: What is the procedure for obtaining a dict from an sqlite query?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use cursor`s fetchall() function and pass it to the dict() function.
---

**Contents**

[TOC]

## Introduction

When working with SQLite databases in Python, it's often useful to retrieve query results as Python dictionaries. This allows us to easily work with the data and perform operations on it. In this guide, we'll explore how to get a dict from SQLite query in Python.


## Step 1: Connect to the database

Before we can retrieve data from an SQLite database, we need to establish a connection. We can use the `sqlite3` library in Python to create a connection object that allows us to interact with the database.

```python
import sqlite3

# Connect to the database
connection = sqlite3.connect('my_database.db')
```


## Step 2: Execute the query

Once we've established a connection, we can execute our query using the `execute()` method of the connection object. This will return a cursor object that we can use to retrieve the results of the query.

```python
# Execute the query
cursor = connection.execute('SELECT * FROM my_table')
```


## Step 3: Fetch the results as a dictionary

By default, the `fetchall()` method of the cursor object returns results as a list of tuples. However, we can use the `fetchall()` method of the `sqlite3.Row` object to retrieve the results as dictionaries. 

```python
# Fetch the results as a dictionary
rows = cursor.fetchall()
results = [dict(row) for row in rows]
```


## Step 4: Close the connection

Once we've retrieved the results of our query, it's important to close the connection to the database using the `close()` method of the connection object.

```python
# Close the connection
connection.close()
```

## Conclusion

By following these steps, we can easily retrieve query results as Python dictionaries when working with SQLite databases in Python. This allows us to quickly and easily work with the data and perform operations on it.
