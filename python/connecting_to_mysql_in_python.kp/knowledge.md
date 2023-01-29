---
title: What is the process for establishing a connection to a MySQL database using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Connect to a MySQL Database in Python by using the mysql.connector library.
---

**Contents**

[TOC]

# Step 1: Install MySQL Connector

Using pip, install the MySQL Connector module. This will allow us to connect to a MySQL database from Python.

```
pip install mysql-connector-python
```

# Step 2: Connect to Database

Use the MySQL Connector module to connect to the database. We will need to provide the hostname, username, password, and database name.

```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="user",
  passwd="password",
  database="mydatabase"
)
```

# Step 3: Create Cursor

Create a cursor object that will allow us to execute SQL commands.

```python
mycursor = mydb.cursor()
```

# Step 4: Execute SQL Commands

We can now execute SQL commands using the cursor object.

```python
mycursor.execute("SELECT * FROM customers")

myresult = mycursor.fetchall()

for x in myresult:
  print(x)
```
