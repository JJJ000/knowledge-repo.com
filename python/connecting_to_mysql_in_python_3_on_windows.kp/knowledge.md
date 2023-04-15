---
title: What is the process of connecting to MySQL in Python 3 on windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can connect to MySQL in Python 3 on Windows by using a MySQL connector like mysql-connector-python module.
---

**Contents**

[TOC]

# Installing MySQL Connector/Python
```
pip install mysql-connector-python
```
This command installs the MySQL Connector/Python module which allows us to make a connection with MySQL.


# Connecting to MySQL
```python
import mysql.connector

mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword"
)

print(mydb)
```
Using the details of the database, the script connects to the MySQL server.


# Executing Queries
```python
mycursor = mydb.cursor()

mycursor.execute("CREATE DATABASE mydatabase")
```
Once the connection is established, queries can be run. This code creates a new database called mydatabase.


# Closing the Connection
```python
mydb.close
```
Once you are done with database operations, it's important to close the connection to MySQL so as to free up system resources.
