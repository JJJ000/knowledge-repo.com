---
title: How to use Python super() with __init__() methods
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Python's super() function allows subclasses to access and call the parent class's \_\_init\_\_() method.
---

**Contents**

[TOC]

### Introduction
Python's `super()` function is a useful tool for accessing inherited methods from a parent or sibling class. It is especially useful when used in combination with the ``__init__`()` method, which is used to initialize an object's state.

### What is super()?
The `super()` function is used to access methods from a parent or sibling class. It allows you to access methods that are inherited from a parent or sibling class without having to explicitly reference the parent or sibling class.

### How is super() used with `__init__`()?
When used in combination with the ``__init__`()` method, `super()` allows you to access methods from the parent or sibling class without having to explicitly reference the parent or sibling class. This is especially useful when initializing an object's state, as it allows you to access the inherited methods without having to explicitly reference the parent or sibling class.

### Conclusion
Python's `super()` function is a useful tool for accessing inherited methods from a parent or sibling class. It is especially useful when used in combination with the ``__init__`()` method, which is used to initialize an object's state. By using `super()` in combination with ``__init__`()`, you can access inherited methods without having to explicitly reference the parent or sibling class.
