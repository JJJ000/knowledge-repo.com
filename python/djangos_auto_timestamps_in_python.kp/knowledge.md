---
title: Django's auto_now and auto_now_add features
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Django auto\_now and auto\_now\_add are model fields that automatically set the value of the field to the current date and time when the object is created or updated, respectively.
---

**Contents**

[TOC]

# What is auto_now and auto_now_add?

auto_now and auto_now_add are two features of the Django ORM (Object-Relational Mapping) that allow for automatically updating a field's value when an object is saved.

# What is auto_now?

auto_now is used to automatically set the value of a DateTimeField to the current date and time whenever an object is saved. This is useful for tracking when an object was last modified.

# What is auto_now_add?

auto_now_add is used to automatically set the value of a DateTimeField to the current date and time when an object is first created. This is useful for tracking when an object was first created.

# How to use auto_now and auto_now_add?

auto_now and auto_now_add can be used in a model definition like this:

```
class MyModel(models.Model):
    created_at = models.DateTimeField(auto_now_add=True)
    modified_at = models.DateTimeField(auto_now=True)
```

When an object of this model is saved, the created_at field will be set to the current date and time and the modified_at field will be updated to the current date and time.
