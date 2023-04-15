---
title: Using python, you can import a csv file into a table in a sqlite3 database
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Python `csv` and `sqlite3` modules to read in the CSV file and insert its data into a table in the SQLite3 database.
---

**Contents**

[TOC]

# Introduction
In this tutorial, we will learn how to import a CSV (comma-separated values) file into a SQLite3 database table using Python. This can be achieved using the SQLite3 module in Python. 

## Prerequisites
The following are the prerequisites for this tutorial:
* Python 3.x installed on your system
* SQLite3 installed on your system

## Approach
We will take the following steps in order to import a CSV file into a SQLite3 database table:

1. Connect to the SQLite3 database using the `sqlite3` module in Python.
2. Create a database table with the same column headers as the CSV file.
3. Open the CSV file in read mode.
4. Read the CSV file line by line and insert the values into the SQLite3 database table.
5. Commit the changes and close the database connection.

# Connecting to the SQLite3 Database
The first step is to connect to the SQLite3 database using the `sqlite3` module in Python. 

```python
import sqlite3

# connect to the database
conn = sqlite3.connect('example.db')
```

Here, `example.db` is the name of the SQLite3 database. If the database doesn't exist, it will be created automatically.

# Creating a Database Table
The next step is to create a database table with the same column headers as the CSV file. 

```python
# create a cursor object
cur = conn.cursor()

# create the table
cur.execute('''
    CREATE TABLE IF NOT EXISTS my_table (
        column_1 TEXT,
        column_2 INTEGER,
        column_3 REAL
    )
''')
```

Here, `my_table` is the name of the database table. You can name it anything you want. `column_1`, `column_2`, and `column_3` are the column headers of the CSV file. The `TEXT`, `INTEGER`, and `REAL` data types are used to define the data types of the columns.

# Reading the CSV File
The next step is to open the CSV file in read mode and read it line by line. 

```python
import csv

# open the CSV file
with open('my_csv_file.csv', 'r') as csv_file:
    reader = csv.reader(csv_file)

    # skip the header row
    next(reader)

    # insert the data into the table
    for row in reader:
        cur.execute('''
            INSERT INTO my_table (column_1, column_2, column_3)
            VALUES (?, ?, ?)
        ''', (row[0], row[1], row[2]))
```

Here, `my_csv_file.csv` is the name of the CSV file. You can use any CSV file you want as long as it has the same column headers as the database table you created earlier.

# Committing the Changes and Closing the Connection
The final step is to commit the changes and close the database connection. 

```python
# commit the changes
conn.commit()

# close the connection
conn.close()
```

This will save the changes made to the SQLite3 database and close the connection.

# Conclusion
In this tutorial, we learned how to import a CSV file into a SQLite3 database table using Python. We used the `sqlite3` module in Python to connect to the SQLite3 database, created a database table, read the CSV file line by line, and inserted the values into the table. Finally, we committed the changes and closed the database connection.
