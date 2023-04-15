---
title: What is the difference between using .filter() and .get() methods in django for retrieving a single object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: .get() is used for retrieving a single object and raises an error if multiple objects are found, while .filter() returns a QuerySet, which can contain multiple objects.
---

**Contents**

[TOC]

Section 1: Introduction
Django is a powerful web framework that allows developers to build complex web applications with ease. One of the most common operations in a web application is retrieving data from a database. Django provides two methods for retrieving a single object from a database: `.filter()` and `.get()`. While both methods accomplish the same task, there are some key differences between the two that developers need to be aware of.

Section 2: Using `.filter()`
The `.filter()` method is used to retrieve one or more objects that meet a specific set of conditions. The method takes a set of keyword arguments that are used to filter the objects based on specific fields in the database table. The method returns a QuerySet, which is a collection of objects that match the specified conditions. If you want to retrieve a single object using `.filter()`, you need to take the first element from the QuerySet. For example:

```python
from myapp.models import MyModel

my_object = MyModel.objects.filter(name='foo').first()
```

In the above example, we are retrieving a single object from the MyModel table where the name field matches the string "foo". We are using the `.first()` method to retrieve the first object from the QuerySet.

Section 3: Using `.get()`
The `.get()` method is used to retrieve a single object that matches a specific set of conditions. The method takes the same set of keyword arguments as `.filter()`, but instead of returning a QuerySet, it returns a single object. If no object is found that matches the specified conditions, a `DoesNotExist` exception is raised. For example:

```python
from myapp.models import MyModel

my_object = MyModel.objects.get(name='foo')
```

In the above example, we are retrieving a single object from the MyModel table where the name field matches the string "foo". If no object is found that matches the specified conditions, a `DoesNotExist` exception is raised.

Section 4: Which to use?
The choice between using `.filter()` and `.get()` to retrieve a single object depends on your specific use case. If you are unsure whether there will be exactly one object that matches the specified conditions, you should use `.filter()` and check the length of the resulting QuerySet. If there is only one object and you are confident that it exists, you can use `.get()` for a more concise syntax. Additionally, if you have a situation where you need to access an attribute of the object that may not exist, you should use `.filter()` to check for the existence of the object before accessing the attribute.
