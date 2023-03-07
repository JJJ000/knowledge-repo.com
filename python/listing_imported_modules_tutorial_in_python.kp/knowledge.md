---
title: What is the method for displaying a catalog of the imported modules?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To list imported modules in Python, use the command `help(`modules`)` in the interactive shell.
---

**Contents**

[TOC]

## Method 1: Using `sys` Module

To list all the imported modules in Python, you can use the `sys` module. It has a list of all the modules currently imported in the interpreter. You can use the `sys.modules` method to get a dictionary of all the imported modules. 

```python
import sys

# Get a list of all imported modules
imported_modules = sys.modules.keys()

# Print the list of modules
print(imported_modules)
```

## Method 2: Using `globals()` Method

Another method to list imported modules in Python is to use the `globals()` method. This method returns a dictionary of all the global variables in the program, including the imported modules.

```python
# Import some modules
import pandas
import numpy

# Get a list of all imported modules
imported_modules = list(filter(lambda x: '__' not in x, globals()))

# Print the list of modules
print(imported_modules)
```

## Method 3: Using `dir()` Method

You can also use the built-in `dir()` method to list all the imported modules in Python. This method lists all the attributes and operations of an object, including the imported modules.

```python
# Import some modules
import pandas
import numpy

# Get a list of all imported modules
imported_modules = [x for x in dir() if isinstance(eval(x), types.ModuleType)]

# Print the list of modules
print(imported_modules)
```

## Method 4: Using `pkgutil` Module

Another alternative to list all the imported modules in Python is to use the `pkgutil` module. This module provides a way to list all the imported modules, including the sub-modules.

```python
import pkgutil

# Get a list of all imported modules
imported_modules = [x for x in pkgutil.iter_modules()]

# Print the list of modules
print(imported_modules)
```
