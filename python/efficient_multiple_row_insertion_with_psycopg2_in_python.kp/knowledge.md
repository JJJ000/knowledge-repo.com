---
title: Insert multiple rows with a single query using psycopg2
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To insert multiple rows with one query in psycopg2, you can use the executemany() function and pass a list of tuples containing the values for each row.
---

**Contents**

[TOC]

Inserting Multiple Rows with one Query using Psycopg2 in Python

Psycopg2 is a popular PostgreSQL database adapter for the Python programming language that allows developers to interact with Postgres databases. Inserting multiple rows into a table in one query can be a faster and more efficient way to update large datasets. In this tutorial, we will explore how to insert multiple rows into a table using Psycopg2 in Python.

1. Creating a list of tuples

The first step in inserting multiple rows into a table is to create a list of tuples containing the values to be inserted. Each tuple in the list represents a single row in the table. For example, if we have a table with columns 'id', 'name', and 'age', we can create a list of tuples like this:
```
users = [(1, 'Alice', 25),
         (2, 'Bob', 30),
         (3, 'Charlie', 35)]
```
2. Writing the SQL query

The next step is to write the SQL query that will insert the data into the table. We can use the Psycopg2 execute_values() method to execute an SQL query that inserts multiple rows at once. The execute_values() method takes two arguments: a cursor object, and a template SQL query string with placeholders for the values to be inserted. The placeholders can be represented by %s or other preferred symbol. Here is an example template query string:
```
query = "INSERT INTO users (id, name, age) VALUES %s"
```
The %s placeholder will be replaced with the values from the list of tuples.

3. Executing the query

After creating the list of tuples and writing the SQL query, the next step is to execute the query using the execute_values() method. Here is an example code to execute the query:
```
import psycopg2

# establish connection
conn = psycopg2.connect(database="mydb", user="myuser", password="mypassword", host="localhost", port="5432")

# create a cursor
cur = conn.cursor()

# list of tuples
users = [(1, 'Alice', 25),
         (2, 'Bob', 30),
         (3, 'Charlie', 35)]

# template query string
query = "INSERT INTO users (id, name, age) VALUES %s"

# execute query
psycopg2.extras.execute_values(cur, query, users)

# commit the transaction
conn.commit()

# close the cursor and connection 
cur.close()
conn.close()
```
4. Conclusion

In conclusion, inserting multiple rows into a table in a single query can be a faster and more efficient way to update large datasets. With Psycopg2, you can easily create a list of tuples containing the values to be inserted, write the SQL query using placeholders, and execute the query using the execute_values() method. This method is particularly useful when working with large datasets, as it minimizes the number of round-trips to the database server.
