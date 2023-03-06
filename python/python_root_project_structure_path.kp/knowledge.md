---
title: How to obtain the root directory of a Python project?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the os module to get the absolute path of the directory containing the script with os.path.abspath(os.path.join(os.path.dirname(\_\_file\_\_), `..`))
---

**Contents**

[TOC]

# Introduction
In Python, it is important to know how to get the path of the root project structure. This can come in handy, especially when working with multiple files, directories, and modules. In this article, we will discuss different methods to get the path of the root project structure in Python.

# Using the __file__ attribute
Python's built-in `__file__` attribute returns the path of the file in which it is called. By using this attribute and navigating through the directory hierarchy, we can get the path of the root project structure.

```python
import os

ROOT_DIR = os.path.dirname(os.path.abspath(__file__)) # This is your Project Root

print(f"Root directory: {ROOT_DIR}")
```

This code will output the path to the root project structure.

# Using the pathlib Module
Python's `pathlib` module provides an object-oriented way of accessing the file system. The `Path` class from this module can be used to get the path of the root project structure.

```python
import pathlib

ROOT_DIR = pathlib.Path(__file__).parent.parent.absolute() # This is your Project Root

print(f"Root directory: {ROOT_DIR}")
```

This code will output the path to the root project structure.

# Using the sys Module
The `sys` module provides information about the Python interpreter and the environment in which it is running. We can use `sys.path` to get the path of the root project structure.

```python
import sys
import os

ROOT_DIR = os.path.dirname(os.path.abspath(sys.argv[0])) # This is your Project Root

print(f"Root directory: {ROOT_DIR}")
```

This code will output the path to the root project structure.

# Conclusion
Knowing how to get the path of the root project structure is essential while working with Python projects. In this article, we discussed three different methods to achieve this - using the `__file__` attribute, the `pathlib` module, and the `sys` module. Choose the method that suits your project best and work with ease!
