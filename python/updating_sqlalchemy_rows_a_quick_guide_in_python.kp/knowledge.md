---
title: What is the process to modify a row entry in sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To update a row entry in SQLAlchemy using Python, use the update() method on the table object, followed by the where() method to specify which row to update, and then the execute() method to run the update query.
---

**Contents**

[TOC]

## Connecting to the Database

The first step to update a row entry in SQLAlchemy is to connect to the database. To do this, we need to import the necessary modules and create an engine object.

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker

# create an engine object
engine = create_engine('postgresql://user:password@localhost/database_name')

# create a session object
Session = sessionmaker(bind=engine)
session = Session()
```

Here, we are creating a PostgreSQL engine object and binding it to a session object.


## Querying the Row for Update

Once we have established a connection to the database, we can query the row that we want to update. This is done using the `query()` method of the session object.

```python
from mymodels import MyTable

# query the row by primary key
row = session.query(MyTable).get(id)
```

Here, `MyTable` is the name of the SQLAlchemy model representing the table we want to update. We can query the row by its primary key using the `get()` method.


## Updating the Row

Once we have queried the row, we can update its attributes using the dot notation. After we have made the desired changes, we can commit the update to the database using the `commit()` method of the session object.

```python
# update the row
row.attribute1 = new_value1
row.attribute2 = new_value2

# commit the changes
session.commit()
```

Here, `attribute1` and `attribute2` are the names of the attributes we want to update. We simply assign new values to these attributes using the dot notation. Once we have made the changes, we can commit them to the database using the `commit()` method.


## Error Handling

It is important to handle errors when updating rows in SQLAlchemy. In case an error occurs, we can use the `rollback()` method of the session object to roll back the changes and ensure that the database remains unchanged.

```python
try:
    # update the row
    row.attribute1 = new_value1
    row.attribute2 = new_value2

    # commit the changes
    session.commit()

except:
    # roll back the changes
    session.rollback()
```

Here, we have placed the update code inside a try-except block. If an error occurs, the except block is executed, which rolls back the changes using the `rollback()` method. This ensures that the database remains unchanged in case of an error.
