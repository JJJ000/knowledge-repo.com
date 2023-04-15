---
title: Can you explain the meaning of *args and **kwargs?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: *args and **kwargs in Python are used to pass a variable number of arguments to a function, where *args represents a tuple of positional arguments and **kwargs represents a dictionary of keyword arguments.
---

**Contents**

[TOC]

## 1. Introduction

In Python, *args and **kwargs are special syntaxes used in function definitions. They allow a function to accept an arbitrary number of positional and keyword arguments, respectively.

## 2. *args

The *args syntax is used for collecting an arbitrary number of positional arguments passed to a function. It is represented by an asterisk (*) followed by a variable name (args, in this case). When the function is called with arguments, all the positional arguments are collected into a tuple and assigned to the variable name.

Here's an example:

```python
def my_sum(*args):
    total = 0
    for num in args:
        total += num
    return total

print(my_sum(1, 2, 3))  # Output: 6
```

## 3. **kwargs

The **kwargs syntax is used for collecting an arbitrary number of keyword arguments passed to a function. It is represented by two asterisks (**) followed by a variable name (kwargs, in this case). When the function is called with keyword arguments, all the keyword arguments are collected into a dictionary and assigned to the variable name.

Here's an example:

```python
def my_func(**kwargs):
    for key, value in kwargs.items():
        print(f"{key} = {value}")

my_func(name="John", age=30, city="New York")
# Output:
# name = John
# age = 30
# city = New York
```

## 4. Using *args and **kwargs together

In a function definition, *args and **kwargs can be used together to accept both positional and keyword arguments. Here's an example:

```python
def my_func(*args, **kwargs):
    for arg in args:
        print(arg)

    for key, value in kwargs.items():
        print(f"{key} = {value}")

my_func(1, 2, 3, name="John", age=30)
# Output:
# 1
# 2
# 3
# name = John
# age = 30
```

In this example, the positional arguments (1, 2, 3) are collected into a tuple named args, and the keyword arguments (name="John", age=30) are collected into a dictionary named kwargs.
