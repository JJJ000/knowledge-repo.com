---
title: How can I determine the data type of a variable in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The canonical way to check for type in Python is to use the built-in isinstance() function.
---

**Contents**

[TOC]

# type() Function
The canonical way to check for type in Python is to use the built-in `type()` function. This function takes a single parameter and returns its type.

# isinstance() Function
Another way to check for type in Python is to use the built-in `isinstance()` function. This function takes two parameters and returns `True` if the first parameter is an instance of the second parameter.

# Subclassing
It is also possible to check for type in Python by subclassing the desired class. This is done by creating a class that inherits from the desired class and overriding the `__init__` method to perform the desired type checking.

# Custom Type Checking
Finally, it is possible to check for type in Python by writing custom type checking functions. This is done by writing a function that takes a single parameter and returns `True` or `False` depending on whether the parameter is of the desired type.
