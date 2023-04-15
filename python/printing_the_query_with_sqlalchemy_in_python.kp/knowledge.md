---
title: Display the exact query using sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To print the actual SQL query in SQLAlchemy, you can use the `print()` function after creating the query object and calling the `statement` attribute of the object.
---

**Contents**

[TOC]

1. Introduction
In SQLAlchemy, it is common to write database queries using the ORM (Object Relational Mapping) syntax. However, there may be situations where it is useful to print the actual SQL query that is being executed by the database engine. This can be especially helpful for debugging purposes or for understanding the performance of a particular query. In this tutorial, we will discuss several approaches to printing the actual query using SQLAlchemy in Python.

2. Using the String Representation
One of the simplest ways to print the actual query in SQLAlchemy is to use the string representation of a query. This can be done by creating an instance of a query object and then printing it. For example:

``` python
from sqlalchemy import create_engine, select, Table, Column, Integer, MetaData

engine = create_engine('sqlite:///example.db')
metadata = MetaData()
user_table = Table('users', metadata,
                   Column('id', Integer, primary_key=True),
                   Column('name', Integer),
                   Column('age', Integer))
conn = engine.connect()

query = select([user_table]).where(user_table.c.age > 25)
print(query)
```

Output:
```
SELECT users.id, users.name, users.age 
FROM users 
WHERE users.age > ?    
```

In this example, we created a basic SQLAlchemy engine and metadata object. We then defined a user_table object and a query that selects all rows from the user_table where the age column is greater than 25. Finally, we printed the query object using the print statement, which displays the actual SQL query that would be executed by the database engine.

3. Enabling SQLAlchemy Logging
Another way to print the actual query in SQLAlchemy is to enable logging. SQLAlchemy includes support for logging, which can be enabled by setting the logging level to a value that includes logging messages for queries. For example:

```python
import logging
from sqlalchemy import create_engine, select, Table, Column, Integer, MetaData

logging.basicConfig()
logging.getLogger('sqlalchemy.engine').setLevel(logging.INFO)

engine = create_engine('sqlite:///example.db')
metadata = MetaData()
user_table = Table('users', metadata,
                   Column('id', Integer, primary_key=True),
                   Column('name', Integer),
                   Column('age', Integer))
conn = engine.connect()

query = select([user_table]).where(user_table.c.age > 25)
result = conn.execute(query)

```

This code creates a basic SQLAlchemy engine and metadata object, and enables basic logging using the logging module. We then define a query that selects all rows from the user_table where the age column is greater than 25. Finally, we execute the query and store the result.

When this code is executed, the SQL query for the query will be printed to the console output as part of the log messages from SQLAlchemy.

4. Using the SQL Expression Compiler
Finally, we can use the SQL Expression Compiler in SQLAlchemy to print the actual query as a string. The SQL Expression Compiler is responsible for converting SQLAlchemy expressions into SQL statements that can be executed by the database engine. To use it to print the actual query, we can call the `compile` method of a SQLAlchemy query object:

```python
from sqlalchemy import create_engine, select, Table, Column, Integer, MetaData

engine = create_engine('sqlite:///example.db')
metadata = MetaData()
user_table = Table('users', metadata,
                   Column('id', Integer, primary_key=True),
                   Column('name', Integer),
                   Column('age', Integer))
conn = engine.connect()

query = select([user_table]).where(user_table.c.age > 25)
print(str(query.compile(compile_kwargs={"literal_binds": True})))
```

In this example, we create a basic SQLAlchemy engine and metadata object and define a user_table object. We then create a query that selects all rows from the user_table where the age column is greater than 25. Finally, we use the `compile` method of the query object to print the actual query as a string.

Note that we pass the `compile_kwargs` argument to the `compile` method to specify literal binds, which will cause the values in the query to be printed as literal values rather than as bound parameters.

Conclusion:
These are some of the ways you can print the actual queries in SQLAlchemy. You can choose to use any of the approaches discussed above depending on your specific use case. Also note that there are other ways that you can use to achieve this. With the knowledge garnered from this tutorial, you can explore other possible ways.
