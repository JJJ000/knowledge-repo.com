---
title: Storing an object (data retention)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Python offers multiple ways to save an object, such as pickling, shelving, and using a database.
---

**Contents**

[TOC]

#1 Using Pickle
Pickle is a module in Python that allows us to serialize objects and store them in a file. This makes it easy to save and load data in Python. To save an object using Pickle, we use the dump() function. This function takes two arguments: the object to be saved and the file object.

#2 Using Shelve
Shelve is another module in Python that allows us to store objects in a file. It uses the dbm database for storage, which is similar to Pickle but more efficient. To save an object using Shelve, we use the open() function. This function takes two arguments: the file name and the access mode.

#3 Using JSON
JSON (JavaScript Object Notation) is a popular data format for storing and exchanging data. It is a text-based format, which makes it easy to read and write. To save an object using JSON, we use the dump() function. This function takes two arguments: the object to be saved and the file object.

#4 Using SQLite
SQLite is a popular database engine that is used to store data in a structured manner. To save an object using SQLite, we use the execute() function. This function takes two arguments: the SQL query and the parameters to be used in the query.
