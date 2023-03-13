---
title: Retrieve the unprocessed post data in Python flask, without consideration of the content-type header
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use request.data instead of request.form to get the raw POST body in Python Flask regardless of Content-Type header.
---

**Contents**

[TOC]

## Introduction
In Python Flask, the `request` object is used to access incoming requests. It provides convenient properties such as `request.form` and `request.json` to parse incoming data. However, these properties are only available if the request has a content type of `application/x-www-form-urlencoded` or `application/json` respectively. If the content type is different or not specified, Flask doesn't parse the request body and `request.form` and `request.json` will be empty. In this article, we will discuss how to get the raw POST body in Flask, regardless of the Content-Type header.

## Using request.data
When the request body is not parsed by Flask, it can be accessed as raw bytes using the `request.data` property. This property is always available and contains the raw POST data. Here's an example of how to access the raw POST data:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/', methods=['POST'])
def parse_request():
    raw_data = request.data.decode('utf-8')
    # do something with the raw data
    return 'Success'
```

In this example, we access the raw POST data using `request.data` and decode it using the `utf-8` encoding. This converts the bytes to a string that can be easily manipulated.

## Using request.get_data()
Similar to `request.data`, Flask provides a method called `request.get_data()` that returns the raw POST data as bytes as well. We can use it like this:

```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/', methods=['POST'])
def parse_request():
    raw_data = request.get_data()
    # do something with the raw data
    return 'Success'
```

In this example, we use `request.get_data()` to get the raw POST data as bytes. This method can also take an optional `as_text` parameter which, when set to `True`, returns a decoded string instead.

## Using @copy_current_request_context
In some cases, Flask may already have parsed the request body but not exposed it through `request.form` or `request.json`. For example, when using Flask-RESTful, the request body is parsed automatically but is not added to `request.form` or `request.json`. In these cases, we can use Flask's `@copy_current_request_context` decorator to access the request body.

```python
from flask import Flask, request
from functools import wraps

app = Flask(__name__)

def get_raw_data(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        with app.request_context(request):
            raw_data = request.data.decode('utf-8')
            # do something with the raw data
        return func(*args, **kwargs)
    return wrapper

@app.route('/', methods=['POST'])
@get_raw_data
def parse_request():
    return 'Success'
```

In this example, we define a decorator called `get_raw_data` that uses `@copy_current_request_context` to access `request.data`. We then use this decorator on our view function to get the raw POST data. This approach requires some extra work, but can be useful in certain situations.

## Conclusion
In this article, we discussed how to get the raw POST body in Flask regardless of the Content-Type header. We explored three methods: using `request.data`, using `request.get_data()`, and using `@copy_current_request_context`. These methods allow us to access the raw POST data as bytes or a decoded string, giving us more flexibility when working with incoming requests.
