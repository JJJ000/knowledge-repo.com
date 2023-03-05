---
title: What is the method for converting sqlalchemy result into json?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the built-in `json.dumps()` function to convert the results of a SqlAlchemy query to JSON format.
---

**Contents**

[TOC]

## Importing required modules

Before we can start serializing SqlAlchemy results to JSON, we need to import the required modules. These include SqlAlchemy itself as well as the json module that we will be using to convert our data to JSON.

```python
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker
import json
```

## Creating an engine and session

To retrieve data using SqlAlchemy, we first need to create an engine and a session. The engine represents our database and the session provides a means of interacting with it.

```python
engine = create_engine('postgresql://username:password@host:port/database')

Session = sessionmaker(bind=engine)
session = Session()
```

## Serializing SqlAlchemy result to JSON

Now that we have our session object, we can use it to retrieve data from our database using SqlAlchemy's query method. We can then convert the resulting object to JSON using Python's json module.

```python
result = session.query(Table).all()
json_result = json.dumps([dict(r) for r in result])
```

In the above code, `Table` refers to the SqlAlchemy table we are querying. We retrieve all records using the `all()` method and convert each row to a dictionary using the `dict()` method. Finally, we use `json.dumps()` to convert the list of dictionaries to JSON format.

## Returning JSON result

Once we have our JSON result, we can return it to the client using whatever method is appropriate for our application. For example, if we are using Flask, we might do something like this:

```python
from flask import jsonify

@app.route('/api/data')
def get_data():
    result = session.query(Table).all()
    json_result = json.dumps([dict(r) for r in result])
    return jsonify(json.loads(json_result))
```

Here, we first convert our SqlAlchemy results to JSON as before, but then we load them back into a Python object using `json.loads()` before returning them using Flask's `jsonify()` function. This ensures that the result is properly formatted as a JSON response.
