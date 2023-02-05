---
title: What is the best way to obtain a list of all the classes within the current module in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the built-in function dir() to get a list of all classes within a current module in Python.
---

**Contents**

[TOC]

### Using dir()

The `dir()` built-in function can be used to get a list of all classes within the current module. 

```python
classes_list = dir(current_module)
```

The `dir()` function returns a list of strings, which are the names of the classes within the module.

### Using inspect

The `inspect` module can also be used to get a list of all classes within the current module. 

```python
import inspect

classes_list = [m[0] for m in inspect.getmembers(current_module, inspect.isclass)]
```

The `inspect.getmembers()` function returns a list of tuples, where the first element of each tuple is the name of the class. The `inspect.isclass` argument can be used to filter out all non-class members from the list.

### Using globals()

The `globals()` built-in function can be used to get a list of all classes within the current module. 

```python
classes_list = [name for name, obj in globals().items() if inspect.isclass(obj)]
```

The `globals()` function returns a dictionary of global variables, which can be filtered using the `inspect.isclass` function to get a list of all classes within the module.
