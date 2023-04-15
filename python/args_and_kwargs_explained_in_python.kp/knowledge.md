---
title: Utilizing *args and **kwargs
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: *args and **kwargs are used to pass a variable number of arguments to a function in Python.
---

**Contents**

[TOC]

## What are *args and **kwargs?
*args and **kwargs are special syntax in Python used to pass a variable number of arguments to a function. *args is used to send a non-keyworded variable length argument list to the function. **kwargs allows you to pass keyworded variable length of arguments to a function. 

## How *args Works
*args can be used when you do not know ahead of time how many arguments will be passed to a function. It allows you to pass a variable number of arguments to a function. The arguments are passed as a tuple and these passed arguments make tuple inside the function with same name as the parameter excluding asterisk *.

## How **kwargs Works
**kwargs works similar to *args, but instead of passing the arguments as a tuple, it passes them as a dictionary. The keyword arguments are passed as a dictionary and these passed arguments make a dictionary inside the function with same name as the parameter excluding double asterisk **.

## Example
The following example demonstrates how *args and **kwargs work.

```
def my_func(*args, **kwargs):
  for arg in args:
    print(arg)
  
  for key, value in kwargs.items():
    print(key, ":", value)
  
my_func("Hello", "World", name="John", age=20)
```

Output:

```
Hello
World
name : John
age : 20
```
