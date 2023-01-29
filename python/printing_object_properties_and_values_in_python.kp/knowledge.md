---
title: Do any of the built-in functions allow for the display of all the properties and values of an object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, there is no built-in function to print all the current properties and values of an object in Python.
---

**Contents**

[TOC]

**No**

### Explanation

Python does not have a built-in function to print all the current properties and values of an object. However, there are several ways to achieve this. 

### Alternatives

One way to print all the current properties and values of an object is to use the `vars()` function. This function returns the __dict__ attribute of the object, which contains all the properties and values of the object.

Another way is to use the `dir()` function. This function returns a list of all the properties and methods of an object.

Finally, you can use the `__dict__` attribute of an object directly to get a dictionary of all the properties and values of the object.
