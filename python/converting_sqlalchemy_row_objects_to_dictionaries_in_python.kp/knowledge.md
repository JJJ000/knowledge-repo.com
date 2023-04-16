---
title: What is the process for transforming a sqlalchemy row object into a Python dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the row object`s keys() and items() methods to create a dict from the row object.
---

**Contents**

[TOC]

### Section 1: Import Libraries

To convert a SQLAlchemy row object to a Python dict, we will need to import the `sqlalchemy` library.

```python
import sqlalchemy
```

### Section 2: Create Connection

Next, we need to create a connection to the database. This can be done using the `create_engine` method.

```python
engine = sqlalchemy.create_engine(<connection_string>)
```

### Section 3: Execute Query

After creating the connection, we can execute our query and get the results as a row object.

```python
result = engine.execute(<query>)
```

### Section 4: Convert to Dict

Finally, we can use the `row2dict` method to convert the row object to a Python dict.

```python
row_dict = row2dict(result)
```
