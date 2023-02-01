---
title: Creating a copy of a dictionary in Python that includes all of the original dictionary's elements and values
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: A deep copy of a dict in Python can be created by using the dict.copy() method or by using the deepcopy() function from the copy module.
---

**Contents**

[TOC]

### Shallow Copy
A shallow copy of a dictionary in Python can be created using the `dict()` constructor. This will create a new dictionary with the same key-value pairs as the original.

### Deep Copy
A deep copy of a dictionary in Python can be created using the `copy.deepcopy()` function. This will create a new dictionary with the same key-value pairs as the original, but will also create new objects for the values, rather than just copying the references.
