---
title: Is there a way to obtain a list of column names from a psycopg2 cursor?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the cursor.description method to get a list of tuples, each containing column name and other metadata.
---

**Contents**

[TOC]

## Introduction
To get a list of column names from a psycopg2 cursor in Python, we need to perform a query on the database and fetch the results from the cursor. The column names can then be extracted from the cursor's description attribute.

## Connect to the DB
First, we need to establish a connection to the database using psycopg2. This requires importing the module and specifying credentials for accessing the desired database.

```python
import psycopg2
conn = psycopg2.connect(database="mydb", user="myuser", password="mypassword", host="localhost", port="5432")
```

## Execute the query and fetch results
Once the connection is established, we can execute a SQL query using the cursor method `execute()` and fetch the results using `fetchall()`. 

```python
cur = conn.cursor()
cur.execute("SELECT column1, column2, column3 FROM mytable")
results = cur.fetchall()
```

## Extract the column names
Finally, we can extract the column names from the cursor's `description` attribute using a list comprehension.

```python
columns = [desc[0] for desc in cur.description]
print(columns)
# Output: ['column1', 'column2', 'column3']
```

With these steps, we have successfully retrieved the column names from a psycopg2 cursor in Python.
