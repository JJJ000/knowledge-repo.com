---
title: What is the methodology to fetch the inserted id once a row has been added to sqlite database through python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use cursor.lastrowid to retrieve the inserted id after inserting a row in SQLite using Python.
---

**Contents**

[TOC]

## Connect to the SQLite database

To retrieve the inserted id after inserting row in SQLite using Python, first we need to connect to the SQLite database. We can use the `sqlite3` module for this purpose. The `connect()` function is used to connect to the database. We need to pass the database name as a parameter to this function.

```python
import sqlite3

# Connect to the SQLite database
conn = sqlite3.connect('database.db')
```

## Create a cursor object

After connecting to the database, we need to create a cursor object that will allow us to execute SQL queries on the database. We can create a cursor object using the `cursor()` function. 

```python
# Create a cursor object
cursor = conn.cursor()
```

## Execute an insert SQL statement

To insert a row into a SQLite table, we can use the `INSERT INTO` SQL statement. 

```python
# SQL statement to insert a row into a table
sql = 'INSERT INTO employees (name, age, salary) VALUES (?, ?, ?)'
params = ('John Doe', 30, 60000)

# Execute the SQL statement
cursor.execute(sql, params)

# Commit the transaction
conn.commit()
```

## Retrieve the inserted id

To retrieve the inserted id, we can use the `lastrowid` property of the cursor object. 

```python
# Retrieve the inserted id
print(f"Employee '{params[0]}' has been inserted with id {cursor.lastrowid}")
```

The `lastrowid` property returns the id of the last row that was inserted into the database. We can use this property to retrieve the id of the row that we just inserted. 

The complete code for retrieving the inserted id after inserting row in SQLite using Python is shown below:

```python
import sqlite3

# Connect to the SQLite database
conn = sqlite3.connect('database.db')

# Create a cursor object
cursor = conn.cursor()

# SQL statement to insert a row into a table
sql = 'INSERT INTO employees (name, age, salary) VALUES (?, ?, ?)'
params = ('John Doe', 30, 60000)

# Execute the SQL statement
cursor.execute(sql, params)

# Commit the transaction
conn.commit()

# Retrieve the inserted id
print(f"Employee '{params[0]}' has been inserted with id {cursor.lastrowid}")

# Close the cursor and connection
cursor.close()
conn.close()
``` 

This code will connect to the SQLite database, insert a row into the `employees` table, retrieve the inserted id, and print it to the console. Finally, it will close the cursor and connection.
