---
title: Compilation of tables, database schema, and dump utilizing the Python sqlite3 api
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The Python `sqlite3` API provides modules and functions to create tables, handle database schema, and dump data for SQLite databases.
---

**Contents**

[TOC]

## Introduction 
In this article, we will learn about how to list tables, the database schema, dump, etc. using the Python sqlite3 API.

## Connecting to the Database
Before we can manipulate the database, it is necessary to connect to it using the Python sqlite3 module. Here is how to establish a connection with a database:
```python
import sqlite3

# Connect to database
conn = sqlite3.connect('my_db.sqlite')
```
In this example, we created a connection object to a database named `my_db.sqlite`. You can replace this with the name of your database.

## Listing tables
Once the connection is made with the database, we can list all tables in the database using the `execute()` method and fetching the required information from the `sqlite_master` table.
```python
# Fetching the tables
res = conn.execute("SELECT name FROM sqlite_master WHERE type='table';")
tables = [table[0] for table in res]

# Printing the tables 
print(f'Tables in the Database: {tables}')
```
Here, we executed the SQL command to fetch all the object names with the type 'table' using the execute() method. The result is stored in a variable named `res`. After that, we created a list comprehension to extract the names of the tables from the result.

## Database Schema
The `PRAGMA` command can be used to access the schema of the database. It provides metadata information about the database. 
```python
res = conn.execute("PRAGMA table_info(table_name);")  

for row in res:  
    print(row) 
```
To access the schema of a table, replace table_name with the name of the table from which you want to get the schema.

## Database Dump
The `sqlite3` module has a method called `iterdump()` that can be used to obtain the entire SQL script of the database. Here is an example of how to use this method and store the dump in a file:
```python
with open('my_db_dump.sql', 'w') as f:
    for line in conn.iterdump():
        f.write(f'{line}\n')
```
In this example, we opened a file called `my_db_dump.sql` to write database dump to it. The `iterdump()` method returns the SQL script line by line, and we write each line to the file using a loop.


## Conclusion
In this article, we learned about how to list tables, the database schema, dump, etc. using the Python sqlite3 API. Using these methods, we can easily access the required information about the database and its objects.
