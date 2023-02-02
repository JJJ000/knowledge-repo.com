---
title: What is the best way to receive posted JSON data in flask?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the request.get\_json() method to access the POSTed JSON in Flask.
---

**Contents**

[TOC]

## Section 1: Setting Up the Flask App

To get POSTed JSON in Flask, the first step is to set up the Flask app. This can be done by importing the Flask library and then creating an instance of the Flask class.

```python
from flask import Flask

app = Flask(__name__)
```

## Section 2: Setting Up the Route

Next, a route should be set up to handle incoming requests. This can be done by using the `@app.route` decorator.

```python
@app.route('/post-json', methods=['POST'])
def post_json():
    pass
```

## Section 3: Retrieving the JSON Data

To retrieve the JSON data from the POST request, the `request` module can be used. The `request.get_json()` method can be used to get the JSON data from the request body.

```python
@app.route('/post-json', methods=['POST'])
def post_json():
    json_data = request.get_json()
```

## Section 4: Processing the JSON Data

Once the JSON data is retrieved, it can be processed as needed. This can be done by accessing the values of the JSON object and performing any necessary operations.

```python
@app.route('/post-json', methods=['POST'])
def post_json():
    json_data = request.get_json()
    # Process the JSON data
    # ...
```
