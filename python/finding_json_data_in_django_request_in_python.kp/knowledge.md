---
title: Can you tell me the location of my JSON data in the django request that I have received?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The JSON data is in the request body of the incoming Django request.
---

**Contents**

[TOC]

# Request object in Django

The Django framework has a request object that carries all the incoming HTTP request data. This object contains all the metadata and data related to the request. 

There are different properties and methods of this request object, which can be used to access different parts of the request, like headers, parameters, request body and more.

# JSON data in the request body

If you're sending JSON data in the request body, you can access it through the request's `body` property. 

In Django, you'll generally receive JSON data through a POST or PUT request with content type set as 'application/json'. This can be accessed by first importing the `json` module and then decoding the body of the request using it.

```python
import json

def my_view(request):
    if request.method == 'POST':
        data = json.loads(request.body)
        # Your JSON data is now in `data` variable
```

# Parsing JSON data through request.POST

In Django, when the incoming `Content-Type` header indicates it’s a form submission (e.g. x-www-form-urlencoded or form-data), you can access the JSON data with Django’s standard `request.POST` attribute.

The `request.POST` object has dictionaries whose key-value pairs correspond to form names and their respective values.

```python
def my_view(request):
    if request.method == 'POST':
        data = request.POST.get('my_json_key')
        # Your JSON data is now in `data` variable
```

# Using serializers to parse JSON data

Django provides serializers to make working with JSON data easier. Django serializers provide abstraction for translating complex data types like Django models and QuerySets into JSON format and vice versa.

To parse JSON data, you can use the `serializers` module and its `loads` function.

```python
from django.core import serializers

def my_view(request):
    if request.method == 'POST':
        data = request.body
        obj = serializers.loads(data, format='json')
        # Your JSON data is now in `obj` variable
```
