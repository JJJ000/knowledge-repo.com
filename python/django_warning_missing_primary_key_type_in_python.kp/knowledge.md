---
title: When a primary key type is not defined, django issues a warning about the use of auto-generated primary keys
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Django warns that it will auto-create a primary key if no primary key type is defined.
---

**Contents**

[TOC]

Section 1: Introduction
Django is a high-level Python web framework that follows the model-view-template (MVT) architectural pattern. It provides built-in support for creating and managing databases using object-relational mapping (ORM). One of the essential aspects of database design is defining primary keys. A primary key uniquely identifies each record in a table and is essential for ensuring data integrity and consistency. However, Django provides an auto-created primary key if a user fails to define a primary key type, which can lead to unforeseen issues.

Section 2: Auto-creating Primary Key Warning
When defining a database table in Django, if a user does not explicitly define a primary key type, the framework will automatically create one. The auto-created primary key is an IntegerField that automatically increments with every new record added to the table. While this feature can be useful, it can also lead to unforeseen issues such as duplicate keys and inefficient index utilization.

In Django, when you do not define a primary key explicitly, you get a warning that looks like this:
```
Auto-created primary key used when not defining a primary key type, by default "django.db.models.AutoField".
```

Section 3: Implications of Using Auto-created Primary Keys
Using auto-created primary keys can lead to some issues in the long run. For instance, auto-created primary keys can lead to inefficient index utilization when many tables start storing data. This can slow down database operations over time, leaving users frustrated with the slow-performing system.

Additionally, auto-generated primary keys can create duplicate keys when data is imported from other sources or when data is added to tables outside of Django's ORM. This can be especially problematic when the importing process spans multiple tables. Eventually, the system might end up with corrupted data, requiring extensive diagnosis and repairs, which can be time-consuming.

Therefore, it is a best practice to avoid auto-created primary keys in Django and define the primary key type explicitly.

Section 4: Conclusion
In conclusion, Django's automatic creation of primary keys feature can be useful, but it can also become problematic in the long run. It can lead to inefficient index utilization, duplicate keys, corrupted data, and other unforeseen issues. For this reason, it is always best practice to explicitly define the primary key type in Django when defining database tables.
