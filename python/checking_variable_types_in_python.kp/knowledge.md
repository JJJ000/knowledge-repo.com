---
title: What is the most efficient way to determine the data type of a Python variable?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The best way to check the type of a Python variable is to use the built-in type() function.
---

**Contents**

[TOC]

# Type Checking with the `type()` Function
The `type()` function is the most idiomatic way to check the type of a Python variable. It returns the type of the variable as a type object. 

# Syntax 
The syntax for the `type()` function is as follows:

```
type(object)
```

# Examples 
Here are some examples of the `type()` function in action:

```
a = 5
type(a)  # Output: <class 'int'>

b = "Hello"
type(b)  # Output: <class 'str'>

c = [1, 2, 3]
type(c)  # Output: <class 'list'>
```
