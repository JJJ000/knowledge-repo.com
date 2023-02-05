---
title: The difference between json.dumps and flask.jsonify in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: json.dumps serializes an object to a JSON formatted string, while flask.jsonify serializes an object to a response object with the application/json mimetype.
---

**Contents**

[TOC]

### json.dumps
json.dumps is a method in the json module of the Python standard library. It is used to convert a Python object into a JSON string. json.dumps takes an object as an argument and returns a string.

### flask.jsonify
flask.jsonify is a function in the Flask web framework. It is used to convert a Python object into a JSON response. flask.jsonify takes an object as an argument and returns a Response object which can be used as an HTTP response.

### Difference
The main difference between json.dumps and flask.jsonify is that json.dumps returns a string, while flask.jsonify returns a Response object. json.dumps is used to convert a Python object into a JSON string, while flask.jsonify is used to convert a Python object into a JSON response.
