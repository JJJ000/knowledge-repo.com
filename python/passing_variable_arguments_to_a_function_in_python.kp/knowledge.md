---
title: Is it possible to pass an unspecified number of arguments to a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, a variable number of arguments can be passed to a function in Python using the *args syntax.
---

**Contents**

[TOC]

## Yes
Python functions can take a variable number of arguments, which are often referred to as *varargs*. Varargs allow a function to be called with an arbitrary number of arguments, and are typically used when the exact number of arguments is unknown.

## How It Works
Varargs are declared by using the `*` operator before the parameter name in the function definition. When the function is called, the arguments are passed in as a tuple. The tuple can then be used inside the function to access the arguments.

## Example
For example, consider the following function definition:
```python
def my_func(*args):
    for arg in args:
        print(arg)
```
This function takes a variable number of arguments and prints each one. It can be called with any number of arguments, like this:
```python
my_func(1, 2, 3, 4, 5)
```
This will print out each of the arguments, one per line:
```
1
2
3
4
5
```

## Benefits
Using varargs can be helpful when the exact number of arguments is unknown or variable. It also allows for easy expansion of the function in the future, as additional arguments can be added without changing the function definition.
