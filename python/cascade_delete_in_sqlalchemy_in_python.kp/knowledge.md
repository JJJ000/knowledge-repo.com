---
title: The process of automatically deleting related records when a parent record is deleted is referred to as "cascade delete" in sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: In SQLAlchemy, cascade delete can be achieved by setting the `cascade` keyword argument to `all`, `delete`, or `delete, all` when defining the relationship between the parent and child tables.
---

**Contents**

[TOC]

Section 1: Understanding Cascade Delete 

In database management systems, deleting a record from a parent table may also require deletion of related records from the child tables. This process is called Cascade Delete, where the deletion operation cascades through related tables and deletes records to maintain referential integrity.

Section 2: Implementing Cascade Delete in SQLAlchemy

SQLAlchemy provides a mechanism to enable cascade delete when defining the relationships between the tables. When defining a relationship, we can set the `cascade` parameter to `delete` or `all`, which will enable cascade delete.

```python
from sqlalchemy.orm import relationship

class Parent(Base):
    __tablename__ = 'parent'
    id = Column(Integer, primary_key=True)
    children = relationship("Child", cascade="all, delete")

class Child(Base):
    __tablename__ = 'child'
    id = Column(Integer, primary_key=True)
    parent_id = Column(Integer, ForeignKey('parent.id'))
```

In the above code, the `relationship` function defines a one-to-many relationship between `Parent` and `Child`. The `cascade` parameter is set to `"all, delete"`, which will propagate all types of changes and delete the child records when the parent record is deleted.

Section 3: Using ON DELETE CASCADE in SQLAlchemy

Another way to enable cascade delete is to set the `ondelete` attribute of the foreign key constraint to `CASCADE`.

```python
from sqlalchemy import ForeignKeyConstraint

class Parent(Base):
    __tablename__ = 'parent'
    id = Column(Integer, primary_key=True)

class Child(Base):
    __tablename__ = 'child'
    id = Column(Integer, primary_key=True)
    parent_id = Column(Integer)
    
    __table_args__ = (ForeignKeyConstraint(['parent_id'], ['parent.id'], ondelete='CASCADE'), {})
```

When the `ondelete` attribute is set to `CASCADE`, deleting a parent record will cause all the associated child records to be deleted automatically.

Section 4: Checking Cascade Delete Behavior

To verify whether cascade delete is working as expected, we can try deleting a parent record and then querying the child table to see if the related records are deleted.

```python
session.query(Parent).filter(Parent.id == 1).delete()
session.commit()

# Verify if related Child records are deleted
children = session.query(Child).filter(Child.parent_id == 1).all()
assert not children
```

The above code will delete the parent record with `id` 1 and verify that there are no child records with `parent_id` as 1. If cascade delete is working correctly, the assertion will pass.
