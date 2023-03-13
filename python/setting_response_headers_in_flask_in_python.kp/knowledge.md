---
title: What is the procedure to establish response headers in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `make\_response()` function to create a response object with desired headers and content, and then return it from the view function.
---

**Contents**

[TOC]

# Introduction
In Flask, you can set response headers using various methods. In this guide, we will be discussing some common methods for setting response headers in Flask.

## Method 1: Using the Response Object
The Flask `Response` object allows you to set headers when generating a response for a client request.

```python
from flask import Flask, Response

app = Flask(__name__)

@app.route('/')
def index():
    response = Response("Hello World")
    response.headers['Custom-Header'] = 'Some value'
    return response
```
In this example, we create a new `Response` object and set its `Custom-Header` key to `Some value`. We then return the response to the client.

## Method 2: Using the @after_request Decorator
Another way to set response headers in Flask is to use the `@after_request` decorator.

```python
from flask import Flask

app = Flask(__name__)

@app.after_request
def add_header(response):
    response.headers['Custom-Header'] = 'Some value'
    return response

@app.route('/')
def index():
    return "Hello World"
```

In this example, we use the `@after_request` decorator to add a `Custom-Header` to the response object. The function that is decorated takes in the response object and adds the header. The response object is then returned to the calling function.

## Method 3: Using Flask's make_response() function
Flask provides the `make_response()` function to create a response object that can be modified before it is returned to the client.

```python
from flask import Flask, make_response

app = Flask(__name__)

@app.route('/')
def index():
    response = make_response("Hello World")
    response.headers['Custom-Header'] = 'Some value'
    return response
```

In this example, we use the `make_response()` function to create a new response object. We then set the `Custom-Header` key to `Some value`. Finally, we return the response object to the client.

## Conclusion
In this guide, we have discussed some common methods for setting response headers in Flask. By using these methods, you can add custom headers to your Flask responses and control how clients interact with your web application.
