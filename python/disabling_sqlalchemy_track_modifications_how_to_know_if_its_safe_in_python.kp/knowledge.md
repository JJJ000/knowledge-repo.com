---
title: Is there a way to determine if it's safe to deactivate sqlalchemy_track_modifications?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can disable SQLALCHEMY\_TRACK\_MODIFICATIONS in Python if you don`t require to track modifications.
---

**Contents**

[TOC]

Introduction 

SQLAlchemy is an open-source SQL toolkit and Object-Relational Mapping (ORM) library that provides a set of high level APIs to create and manipulate database records. SQLAlchemy_TRACK_MODIFICATIONS is an optional feature, which is used to keep track of the modifications made to the database records. In this article, we will discuss the conditions for disabling SQLAlchemy_TRACK_MODIFICATIONS in Python.

1. What is SQLALCHEMY_TRACK_MODIFICATIONS?

SQLALCHEMY_TRACK_MODIFICATIONS is a configuration variable in SQLAlchemy, which is used to track the modifications made to the database records. When this feature is enabled, SQLAlchemy keeps track of changes made to the database by using event listeners. This feature is useful for database management and debugging purposes.

2. When should I disable SQLALCHEMY_TRACK_MODIFICATIONS?

SQLALCHEMY_TRACK_MODIFICATIONS can be disabled for performance improvement purposes. Disabling this feature is particularly useful when working with large datasets, as it can significantly reduce the overhead associated with tracking the changes made to the database.

However, it is important to note that disabling this feature may result in unexpected behavior, particularly when working with database sessions. For instance, disabling this feature may cause session.commit() to fail when the database record is modified, but the modification is not tracked by SQLAlchemy.

3. How do I disable SQLALCHEMY_TRACK_MODIFICATIONS?

Disabling SQLALCHEMY_TRACK_MODIFICATIONS can be done by setting it to False while initializing the application instance. Here is an example of how it can be done:

```python
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False
db = SQLAlchemy(app)
```

It is important to note that disabling this feature may cause unexpected behavior, particularly when working with database sessions. Therefore, it is advisable to test the application after disabling SQLAlchemy_TRACK_MODIFICATIONS to ensure that there are no unexpected consequences.

4. Conclusion

In conclusion, SQLALCHEMY_TRACK_MODIFICATIONS is an optional feature in SQLAlchemy, which is used to track the modifications made to the database records. This feature can be disabled for performance improvement purposes. However, disabling this feature may result in unexpected behavior, particularly when working with database sessions. Therefore, it is important to test the application after disabling SQLAlchemy_TRACK_MODIFICATIONS to ensure that there are no unexpected consequences.
