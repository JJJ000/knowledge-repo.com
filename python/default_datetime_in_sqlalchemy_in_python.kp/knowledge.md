---
title: The default datetime in sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The default DateTime in SQLAlchemy is the current date and time at the moment the field is declared.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
SQLAlchemy is a Python library which provides a set of high-level API for working with relational databases. One of the most common tasks in working with databases is inserting data into tables. When inserting data into a table, one might want to set a default value for a column, in case the data for that column is not provided. In this article, we will discuss how to set default DateTime in SQLAlchemy.


Section 2: What is a DateTime column in SQL?
-------------------------------------------
A DateTime column in SQL is a column that stores date and time values. This type is commonly used to store timestamps when a record was created, or when a certain event happened. In SQLAlchemy, the DateTime column is represented by the `DateTime` type.


Section 3: Setting default DateTime in SQLAlchemy
-------------------------------------------------
To set a default DateTime value in SQLAlchemy, we can use the `default` parameter of the column constructor. Here is an example:

```python
from sqlalchemy import Column, DateTime, func

class MyTable(Base):
    __tablename__ = 'my_table'
    id = Column(Integer, primary_key=True)
    created_at = Column(DateTime, default=func.now())
```

In this example, we define a table called `MyTable` with an `id` column and a `created_at` column. For the `created_at` column, we set the default value to the current timestamp using the `func.now()` function provided by SQLAlchemy.


Section 4: Conclusion
---------------------
In this article, we discussed how to set default DateTime in SQLAlchemy. We learned that the DateTime column in SQL is a column that stores date and time values and that in SQLAlchemy, the DateTime column is represented by the `DateTime` type. We also saw how to set a default DateTime value in SQLAlchemy using the `default` parameter of the column constructor.
