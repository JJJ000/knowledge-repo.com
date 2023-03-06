---
title: Reword "ensuring uniqueness across multiple columns using sqlalchemy."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To ensure uniqueness across multiple columns in SQLAlchemy, use the `UniqueConstraint` constraint on the table definition.
---

**Contents**

[TOC]

Check your Database Constraints
---

Before diving into the code, it's important to double-check that your database constraints include the unique requirement across the columns you need. SQLAlchemy will work with the constraints you defined in the database, so it's important to ensure the database is setup properly before writing any code.

Using UniqueConstraint
---

Assuming that the database has been properly setup with the unique constraint, you can enforce the constraint in SQLAlchemy by using the `UniqueConstraint` class in your model definition. Here is an example:

```python
from sqlalchemy import UniqueConstraint

class MyModel(Base):
    __tablename__ = 'my_table'
    id = Column(Integer, primary_key=True)
    column_a = Column(String(255))
    column_b = Column(String(255))
    
    __table_args__ = (UniqueConstraint('column_a', 'column_b'), )
```

Note how the `__table_args__` tuple includes an instance of `UniqueConstraint` that specifies the columns on which to enforce the unique constraint.

Using Index
---

Another way to enforce unique constraint across multiple columns is using Index in Model definition. Here is an example:

```python
from sqlalchemy import Index

class MyModel(Base):
    __tablename__ = 'my_table'
    id = Column(Integer, primary_key=True)
    column_a = Column(String(255))
    column_b = Column(String(255))

    __table_args__ = (
        Index('idx_my_table_column_a_column_b', column_a, column_b, unique=True),
    )
```

Here, we are using `Index` class to create an index and set the unique property to true, so it will enforce the unique constraint across columns.

Using event.listen()
---

If you want to implement the unique constraint check yourself, you can do so by using the `event.listen()` method to intercept the inserts and updates to the database. Here is an example:

```python
from sqlalchemy import event, exc

class MyModel(Base):
    __tablename__ = 'my_table'
    id = Column(Integer, primary_key=True)
    column_a = Column(String(255))
    column_b = Column(String(255))

@event.listens_for(MyModel, 'before_insert')
@event.listens_for(MyModel, 'before_update')
def check_unique_constraint(mapper, connection, target):
    q = connection.query(MyModel).filter(
        MyModel.column_a == target.column_a,
        MyModel.column_b == target.column_b
    )
    if q.count() > 0:
        raise exc.IntegrityError('Combination of column_a and column_b must be unique')
```

Here we are using the `event.listen()` method to listen for insert and update events. When a new record is attempting to be inserted or updated, we query the database to see if the combination of `column_a` and `column_b` already exists, and if so, we raise an `IntegrityError` to prevent the operation.
