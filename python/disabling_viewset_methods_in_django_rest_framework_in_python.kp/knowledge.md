---
title: In the django-rest-framework, how to turn off a method in a viewset?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Add the decorator @swagger\_ignore or @decorators.action(methods=[`post`], detail=True) above the method in the ViewSet class.
---

**Contents**

[TOC]

## 1. Introduction
Django REST framework is a popular third-party package for building APIs using Django. It provides a simple and powerful approach for building APIs. In this tutorial, we'll look at how to disable a method in a ViewSet using DRF. In particular, we'll look at how to disable the `create` method in a ViewSet.

## 2. Disabling Methods in a ViewSet
To disable a method in a ViewSet, we can subclass the ViewSet and override the method we wish to disable. In our case, we wish to disable the `create` method, which is used to create new instances of the model. Here's how to do it:

```python
from rest_framework import viewsets

class MyViewSet(viewsets.ModelViewSet):
    ...
    def create(self, *args, **kwargs):
        raise MethodNotAllowed("create")
```

In the code above, we subclassed the `ModelViewSet` class and overrode its `create` method. Instead of creating a new instance of the model, we raised a `MethodNotAllowed` exception.

## 3. Using Decorators to Disable Methods
Another way to disable a method in a ViewSet is to use a decorator. We can define a decorator that raises a `MethodNotAllowed` exception when applied to a method. Here's how to do it:

```python
from rest_framework.exceptions import MethodNotAllowed
from rest_framework.decorators import action

def disable_methods(*methods):
    def decorator(func):
        def wrapper(*args, **kwargs):
            if all(method not in methods for method in args[1].data.keys()):
                return func(*args, **kwargs)
            raise MethodNotAllowed(",".join(methods))
        return wrapper
    return decorator

class MyViewSet(viewsets.ModelViewSet):
    ...
    @disable_methods("create")
    @action(detail=False, methods=["post"])
    def bulk_create(self, request, *args, **kwargs):
        ...
```

In the code above, we defined the `disable_methods` decorator that takes a list of method names as arguments. It returns a new decorator that checks if any of the specified methods are used in the request data. If any of the methods are used, it raises a `MethodNotAllowed` exception. We then applied this decorator to the `bulk_create` method of our ViewSet, effectively disabling the `create` method.
  
## 4. Conclusion
In this tutorial, we saw how to disable a method in a ViewSet using Django REST framework. We can achieve this by subclassing the ViewSet and overriding the method, or by using a decorator to check if the method is used in the request data. Disabling methods can be useful in cases where we want to prevent users from performing certain actions on our resources.
