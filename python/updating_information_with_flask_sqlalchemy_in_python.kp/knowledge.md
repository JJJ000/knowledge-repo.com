---
title: Updating information of a row using flask-sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To update a row`s information in Flask-SQLalchemy, you need to query the row, modify the values, then commit the changes using the db.session.commit() method.
---

**Contents**

[TOC]

# Introduction

Flask-SQLAlchemy is a Python library that integrates Flask and SQLAlchemy, a popular Object Relational Mapping (ORM) toolkit. It provides developers with an easy-to-use interface to interact with databases using Python code. Updating a row's information is an important part of managing data in a database. Flask-SQLAlchemy provides several ways to update a row's information.

# Retrieving a Row

Before updating a row's information, you need to retrieve the row from the database. Flask-SQLAlchemy provides several ways to retrieve a row, depending on your needs. The most common way is to use the `query` method of the model class.

```python
row = Model.query.get(id)
```

This retrieves the row with the given `id` from the database. You can also use `filter_by` to retrieve rows based on specific criteria.

```python
rows = Model.query.filter_by(column=value).all()
```

# Updating a Row

Once you have retrieved the row from the database, you can update its information by modifying its attributes and calling the `commit` method of the SQLAlchemy session.

```python
row.column = new_value
db.session.commit()
```

This updates the `column` of the row to `new_value`. You can also update multiple columns at once.

```python
row.column1 = new_value1
row.column2 = new_value2
db.session.commit()
```

This updates both `column1` and `column2` of the row to `new_value1` and `new_value2`, respectively.

# Updating Multiple Rows

To update multiple rows at once, you can use the `update` method of the `query` object.

```python
Model.query.filter_by(column=value).update({column: new_value})
db.session.commit()
```

This updates all rows with `column` equal to `value` to have `column` equal to `new_value`. You can also update multiple columns at once.

```python
Model.query.filter_by(column=value).update({column1: new_value1, column2: new_value2})
db.session.commit()
```

This updates all rows with `column` equal to `value` to have `column1` equal to `new_value1` and `column2` equal to `new_value2`.
