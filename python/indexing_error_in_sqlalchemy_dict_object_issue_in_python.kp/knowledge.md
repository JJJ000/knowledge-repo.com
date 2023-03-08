---
title: The error message from sqlalchemy is unusual it indicates a typeerror with the message "dict" object cannot be indexed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: This error occurs when trying to index a dictionary object in a way that is not supported, which may indicate a syntax error or incorrect use of the object.
---

**Contents**

[TOC]

Section 1: Explanation of SQLAlchemy

SQLAlchemy is a Python toolkit and an Object-Relational Mapping (ORM) library that provides a set of high-level API for connecting to relational databases. SQLAlchemy can be used for SQL expressions, schema creation, and session management, among other things. It contains several features that let developers interact with databases in a more Pythonic way.

Section 2: IndexError vs TypeError

IndexError and TypeError are two common Python errors. An IndexError happens when the index used to access a sequence is out of range, while a TypeError occurs when an operation or function is performed on an object of an inappropriate type. When you try to index a dict object as a list, you will encounter a TypeError since dictionaries don't support indexing as lists do. 

Section 3: Possible Cause of the Error Message

The error message, "TypeError: 'dict' object does not support indexing," can occur when using SQLAlchemy if you try to access a dictionary object as if it is a list object. This could happen in your code if you are using a dictionary to map to a SQL database table, and you are trying to access values in the dictionary using an index rather than by the key.

Section 4: Solution to the Error Message

To fix the "TypeError: 'dict' object does not support indexing" error in SQLAlchemy, you need to replace the index with the key-value pair. Instead of accessing the dictionary with an index, use the key-value pair instead. If you were trying to access a value in the dictionary using an index, replace it with the key that maps to the value. For example, if you have a dictionary with the key "name" and value "John," you can access the value using "dict_name['name']" instead of "dict_name[0]".
