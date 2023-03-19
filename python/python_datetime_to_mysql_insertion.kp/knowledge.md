---
title: How to add a Python datetime.datetime object into mysql?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To insert a Python datetime.datetime object into MySQL, you should use parameterized queries with placeholders and pass the datetime object as a parameter.
---

**Contents**

[TOC]

## Introduction
MySQL is a widely used relational database management system, while Python is a very popular programming language. Whenever we work with both of these, there may be a need to insert Python datetime values into MySQL. In this tutorial, we will learn how to perform such an operation. 

## Establishing a MySQL Connection
To insert Python datetime values into MySQL, we first need to create a connection to the MySQL database. The first thing we have to do is to open the connection using the connect() function.

```python
import mysql.connector
from mysql.connector import Error

try:
    connection = mysql.connector.connect(
        host='localhost',
        database='test_database',
        user='root',
        password='password'
    )
    if connection.is_connected():
        print('Connected to MySQL database')
        
except Error as e:
    print('Error while connecting to MySQL', e)
```

## Inserting Python DateTime Object into MySQL
After establishing the connection, we can insert our datetime values into MySQL. Suppose we have a Python datetime object, "my_datetime", which we want to insert into a MySQL table. We can insert a datetime value into MySQL using the query shown below:

```python
from datetime import datetime

my_datetime = datetime.now()

my_query = "INSERT INTO my_table (my_datetime_column) VALUES (%s)"

cursor = connection.cursor()
cursor.execute(my_query, (my_datetime,))
connection.commit()

print(cursor.rowcount, 'Record inserted successfully into my_table.')
```

Here, we first import the Python datetime module, then we create a Python datetime object using the now() function. We then insert the datetime value into MySQL using the query mentioned above. Finally, we commit the changes to the database.

## Closing the MySQL Connection
It is important to close the MySQL connection once we are done with it. We can close the connection by calling the close() function. 

```python
if connection.is_connected():
    cursor.close()
    connection.close()
    print('MySQL connection closed successfully.')
```
Here, we simply check if the connection is still open, then we close the cursor and connection before printing a message to confirm our connection was closed.

## Conclusion
This tutorial has shown how to insert a Python datetime object into MySQL. We have learned how to establish a connection to the MySQL database, how to insert a datetime value into MySQL, and how to close the connection once we are finished with it.
