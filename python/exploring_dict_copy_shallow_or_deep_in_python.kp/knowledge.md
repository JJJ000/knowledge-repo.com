---
title: What type of copy is dict.copy() - shallow or deep?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: dict.copy() is a shallow copy in Python.
---

**Contents**

[TOC]

# Shallow Copy
A shallow copy is a bit-wise copy of an object. It copies the object’s reference pointers just like a regular assignment statement. A shallow copy creates a new object which stores the reference of the original elements.

# Deep Copy
A deep copy is a bit-wise copy of an object and its sub-objects. It copies the objects and all its sub-objects, making copies of each object. A deep copy creates a new object and recursively adds the copies of the child objects to it.
