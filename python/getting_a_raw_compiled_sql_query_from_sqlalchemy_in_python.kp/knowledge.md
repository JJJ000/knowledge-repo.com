---
title: What is the method to obtain an unprocessed, compiled sql statement from a sqlalchemy expression?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To get the raw SQL query from a SQLAlchemy expression in Python, use the `str()` method on the query object to print the query as a string.
---

**Contents**

[TOC]

Preparing the environment
To get the raw, compiled SQL query from a SQLAlchemy expression in Python, you'll need to perform the following steps:

1. Install SQLAlchemy:

```python
!pip install SQLAlchemy
```

2. Import the required libraries:

```python
from sqlalchemy import create_engine, MetaData, Table, Column, Integer, String
from sqlalchemy.sql import select, text
```

Creating the database table:

1. Define the table structure:

```python
metadata = MetaData()

users = Table('users', metadata,
    Column('id', Integer, primary_key=True),
    Column('name', String),
    Column('age', Integer),
    Column('email', String),
)
```

2. Create the database:

```python
engine = create_engine('sqlite:///users.db', echo=True)
metadata.create_all(engine)
```

Executing a SQL query:

1. Define the query:

```python
stmt = select([users]).where(users.c.age > 25)
```

2. Compile and execute the query:

```python
result = engine.execute(stmt)

for row in result:
    print(row)
```

The output will display all rows where the age is greater than 25.

Getting the raw, compiled SQL query:

1. Define the query:

```python
stmt = select([users]).where(users.c.age > 25)
```

2. Get the raw, compiled SQL query:

```python
query = str(stmt.compile(engine, compile_kwargs={"literal_binds": True}))
print(query)
```

This will output the raw, compiled SQL query in the following format:

```
SELECT users.id, users.name, users.age, users.email 
FROM users 
WHERE users.age > 25
```
