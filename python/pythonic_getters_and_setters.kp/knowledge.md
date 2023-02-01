---
title: What is the most efficient way to use getters and setters in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The pythonic way to use getters and setters is to use the @property decorator.
---

**Contents**

[TOC]

**Getters**

1. Use the `@property` decorator: 
   The `@property` decorator allows you to define a method that can be used like an attribute. When the method is called, it will return the value of the attribute.

2. Use the `getattr()` method:
   The `getattr()` method can be used to get the value of an attribute. It takes two arguments, an object and the name of the attribute.

**Setters**

1. Use the `@property` decorator: 
   The `@property` decorator allows you to define a method that can be used like an attribute. When the method is called, it will set the value of the attribute.

2. Use the `setattr()` method:
   The `setattr()` method can be used to set the value of an attribute. It takes three arguments, an object, the name of the attribute, and the value to be set.
