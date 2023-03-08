---
title: Perform an insertion in mongodb only if the object does not already exist
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: In MongoDB with pymongo, you can use the `update\_one()` method with `upsert=True` to insert a document if it does not already exist.
---

**Contents**

[TOC]

Checking if the Document Exists
---

Before inserting a document, we need to check if the document already exists in the collection. We can check this by using the `count_documents()` method, which returns the number of documents that match a given filter.

Here's an example:

```python
from pymongo import MongoClient

client = MongoClient()
db = client['mydb']
collection = db['mycollection']

document = {'name': 'Alice', 'age': 25}

if collection.count_documents(document) == 0:
    # The document does not exist, insert it
    collection.insert_one(document)
```

In this example, we create a MongoClient object and get a database and collection object. We define a document we want to insert and then check if it exists in the collection using `count_documents()`. If there are no documents that match the `document` filter, we insert it using the `insert_one()` method.

Inserting the Document if it Doesn't Exist
---

Now that we know how to check if a document exists, we can proceed to insert it if it doesn't. One way to accomplish this is by using the `update_one()` method with the `upsert` option.

```python
from pymongo import MongoClient

client = MongoClient()
db = client['mydb']
collection = db['mycollection']

document = {'name': 'Alice', 'age': 25}

collection.update_one(document, {'$set': document}, upsert=True)
```

In this example, we use the `update_one()` method to update the first document that matches the `document` filter. The second argument to `update_one()` specifies the update operation, which is to replace the existing document with the new `document`. The `upsert` option is set to `True`, which tells MongoDB to insert the `document` if there are no documents that match the filter.

Using the `insert_one()` Method with a Try-Except Block
---

Another way to insert a document if it doesn't exist is by using the `insert_one()` method within a try-except block. Here's an example:

```python
from pymongo import MongoClient
from pymongo.errors import DuplicateKeyError

client = MongoClient()
db = client['mydb']
collection = db['mycollection']

document = {'name': 'Alice', 'age': 25}

try:
    collection.insert_one(document)
except DuplicateKeyError:
    # The document already exists, do nothing
    pass
```

In this example, we try to insert the `document` using `insert_one()`. If there's a duplicate key error, it means that the document already exists, so we catch the error and do nothing.
