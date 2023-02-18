---
title: Convert a sql table to JSON format using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The result of a SQL query can be converted to a JSON object in Python using the json.dumps() function.
---

**Contents**

[TOC]

## Section 1: Creating SQL Table

In order to create a SQL table in Python, we must first define the table structure. This is done by creating a CREATE TABLE statement in SQL. The syntax for this statement is:

```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
    ...
);
```

For example, if we wanted to create a table called `users` with three columns: `id`, `name`, and `email`, we could use the following statement:

```
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name VARCHAR(255),
    email VARCHAR(255)
);
```

## Section 2: Inserting Data into the Table

Once we have created the table, we can then insert data into it. This is done using an INSERT statement in SQL. The syntax for this statement is:

```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

For example, if we wanted to insert a new user into our `users` table, we could use the following statement:

```
INSERT INTO users (name, email)
VALUES ('John Doe', 'john@example.com');
```

## Section 3: Querying the Table

Once we have inserted data into the table, we can then query the data using a SELECT statement in SQL. The syntax for this statement is:

```
SELECT column1, column2, column3, ...
FROM table_name
WHERE condition;
```

For example, if we wanted to retrieve all users from our `users` table, we could use the following statement:

```
SELECT *
FROM users;
```

## Section 4: Converting the Table to JSON

Finally, once we have queried the table, we can then convert the table data to JSON format using the Python library `json`. The syntax for this is:

```
import json

data = cursor.fetchall()
json_data = json.dumps(data)
```

Where `cursor` is a SQL cursor object. This will convert the table data into a JSON string which can then be used in other applications.
