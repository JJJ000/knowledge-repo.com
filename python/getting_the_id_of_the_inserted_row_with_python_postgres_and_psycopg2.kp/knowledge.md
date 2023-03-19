---
title: How to retrieve the id of a row recently inserted using python, postgres, and psycopg2?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `RETURNING` clause in the INSERT statement and then fetch the result using `fetchone()` or `fetchall()` from the cursor object.
---

**Contents**

[TOC]

## Setting up the Connection

First, we need to set up the connection to our PostgreSQL database. We'll be using the `psycopg2` library for this. Here's how you can do it:

```python
import psycopg2

conn = psycopg2.connect(
    host="myhost",
    database="mydatabase",
    user="myusername",
    password="mypassword"
)
```

Replace the `host`, `database`, `user`, and `password` values with your own values.

## Inserting Data into the Table

Next, we'll insert some data into a table in our database. Let's assume we have a table called `users` with columns `id`, `name`, and `email`.

```python
cur = conn.cursor()

cur.execute("""
    INSERT INTO users (name, email)
    VALUES ('John Doe', 'johndoe@example.com')
""")
```

This will insert a new row into the `users` table with `name` set to `"John Doe"` and `email` set to `"johndoe@example.com"`.

## Retrieving the ID of the Inserted Row

Finally, we can retrieve the ID of the inserted row. PostgreSQL has a function called `lastval()` that returns the value of the most recently used *sequence* in the current session. When we insert a row with a serial ID column (i.e. a column with the `SERIAL` or `BIGSERIAL` data type), a sequence is automatically created to provide unique values for that column.

Here's how we can use `lastval()` to retrieve the ID of the row we just inserted:

```python
cur.execute("SELECT lastval()")
row_id = cur.fetchone()[0]

print("Inserted row with ID:", row_id)
```

This will print out the ID of the row that was just inserted. 

## Committing the Changes

Don't forget to commit the changes you made:

```python
conn.commit()
```

This will save the changes to the database.
