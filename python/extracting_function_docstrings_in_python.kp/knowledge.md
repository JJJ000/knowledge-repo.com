---
title: Retrieving the function's docstring
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The docstring of a Python function can be obtained using the built-in `doc` attribute or the `help` function.
---

**Contents**

[TOC]

## Introduction

In Python, every function can have a brief summary of its operation written as a docstring. The docstring is usually enclosed in triple quotes (""") and placed below the function definition. In this article, we will discuss different ways to get the docstring from a function in Python.

## Using __doc__ attribute

The simplest way to get the docstring of a function is by using the __doc__ attribute. The __doc__ attribute contains the docstring of the function as a string.

```python
def add(x, y):
    """
    This function adds two numbers.
    """
    return x + y

print(add.__doc__)
```

Output:
```
This function adds two numbers.
```

## Using help() function

Another way to get the docstring of a function is by using the help() function. The help() function returns a formatted help page for the specified object, which includes the docstring.

```python
def add(x, y):
    """
    This function adds two numbers.
    """
    return x + y

help(add)
```

Output:
```
Help on function add in module __main__:

add(x, y)
    This function adds two numbers.
``` 

## Using inspect module

The inspect module provides several useful functions and classes to help us get information about live objects such as modules, classes, methods, functions, etc. We can use the getdoc() function of the inspect module to get the docstring of a function.

```python
import inspect

def add(x, y):
    """
    This function adds two numbers.
    """
    return x + y

print(inspect.getdoc(add))
```

Output:
```
This function adds two numbers.
```

## Conclusion

In this article, we discussed different ways to get the docstring of a function in Python. We can use the __doc__ attribute, the help() function, or the getdoc() function of the inspect module to get the docstring.
