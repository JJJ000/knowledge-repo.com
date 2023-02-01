---
title: Send a JSON response from a flask view
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: A Flask view can return a JSON response by using the jsonify() function from the Flask library.
---

**Contents**

[TOC]

## Using jsonify

The Flask framework provides a convenient way to return JSON responses using its `jsonify` method. This method takes a Python dictionary as an argument and returns a JSON response.

```python
from flask import jsonify

@app.route('/api/data')
def get_data():
    data = {'name': 'John Doe', 'age': 42}
    return jsonify(data)
```

## Using Response

Alternatively, you can use the `Response` object from Flask to return a JSON response. This method takes a JSON-serialized string as an argument and returns a response with the appropriate content type.

```python
from flask import Response
import json

@app.route('/api/data')
def get_data():
    data = {'name': 'John Doe', 'age': 42}
    return Response(json.dumps(data), mimetype='application/json')
```

## Using make_response

You can also use the `make_response` method from Flask to return a JSON response. This method takes a response object and a JSON-serialized string as arguments and returns a response with the appropriate content type.

```python
from flask import make_response
import json

@app.route('/api/data')
def get_data():
    data = {'name': 'John Doe', 'age': 42}
    response = make_response(json.dumps(data))
    response.mimetype = 'application/json'
    return response
```
