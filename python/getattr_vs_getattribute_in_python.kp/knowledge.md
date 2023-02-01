---
title: What is the distinction between __getattr__ and __getattribute__?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: \_\_getattr\_\_ is called when an attribute is not found in the instance, while \_\_getattribute\_\_ is called for every attribute access.
---

**Contents**

[TOC]

#### __getattr__
The `__getattr__` method is called when an attribute lookup has not found the attribute in the usual places (i.e. it is not an instance attribute nor is it found in the class tree for self). This method should return the (computed) attribute value or raise an `AttributeError` exception.

#### __getattribute__
The `__getattribute__` method is called unconditionally to implement attribute accesses for instances of the class. It is called even when the attribute is not found. This method should return the (computed) attribute value or raise an `AttributeError` exception.

#### Difference
The main difference between `__getattr__` and `__getattribute__` is that `__getattr__` is only called when an attribute is not found, while `__getattribute__` is called unconditionally to implement attribute accesses. `__getattr__` is also called if the attribute is not found in the instance (but is found in the class tree). `__getattribute__` is not called if the attribute is not found in the instance.
