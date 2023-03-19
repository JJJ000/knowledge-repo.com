---
title: Is there a way to incorporate uuids with sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To use UUIDs in SQLAlchemy in Python, you need to import the UUID type from the sqlalchemy.dialects.postgresql package and specify it as the type of the UUID column in your table definition.
---

**Contents**

[TOC]

## Introduction
UUID stands for Universal Unique Identifier. It is a 128-bit value represented by a string of hexadecimal characters. SQLAlchemy is a popular Object Relational Mapper (ORM) for Python. This article will explain how to use UUIDs in SQLAlchemy in Python.

## Install the UUID package
Before using UUIDs in SQLAlchemy, we need to install the Python `uuid` package. The `uuid` module provides UUID objects (the `UUID` class) and various functions to generate unique identifiers.

To install the `uuid` package, run the following command:

```
pip install uuid
```

## Define a UUID column in the model 
To use UUIDs in SQLAlchemy, we need to define a UUID column in the model. We can use the `sqlalchemy.dialects.postgresql.UUID` data type for PostgreSQL or `sqlalchemy.types.String` for other databases.

Example:

```python
from sqlalchemy import Column, String
from sqlalchemy.dialects.postgresql import UUID
import uuid

class MyModel(Base):
    __tablename__ = 'my_table'

    id = Column(UUID(as_uuid=True), primary_key=True, default=uuid.uuid4)
    name = Column(String)
```

In the above example, we define a UUID column (`id`), which is the primary key of the table. The `as_uuid=True` argument tells SQLAlchemy to use the `uuid.UUID` class to represent the UUID. The `default` argument generates a new UUID value for each new row.

## Query with UUIDs
To query with UUIDs in SQLAlchemy, we need to create a UUID object and pass it as a parameter to the query.

Example:

```python
my_uuid = uuid.UUID('123e4567-e89b-12d3-a456-426614174000') # create a UUID object
result = session.query(MyModel).filter(MyModel.id == my_uuid).all() # query with UUID
```

In the above example, we create a UUID object with the string value `123e4567-e89b-12d3-a456-426614174000` and use it to filter the query on the `id` column.

## Conclusion
In this article, we learned how to use UUIDs in SQLAlchemy in Python. We installed the `uuid` package, defined a UUID column in the model, queried with UUIDs, and hopefully gained a deeper understanding of how UUIDs can be used in SQLAlchemy applications.
