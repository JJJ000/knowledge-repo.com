---
title: What is the type of a Python variable?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The type of a Python variable can be determined using the type() function.
---

**Contents**

[TOC]

# Using type()

Python has a built-in function called `type()` which returns the type of the variable passed to it.

```python
def determine_type(variable):
    return type(variable)
```

# Examining the Value

In some cases, it may be possible to determine the type of a variable by examining its value. For example, if a variable holds an integer value, it is likely of type `int`.

```python
def determine_type(variable):
    if isinstance(variable, int):
        return "int"
```

# Using isinstance()

The `isinstance()` function can be used to check if an object is an instance of a particular type.

```python
def determine_type(variable):
    if isinstance(variable, int):
        return "int"
    elif isinstance(variable, str):
        return "str"
    elif isinstance(variable, list):
        return "list"
    # ...
```
