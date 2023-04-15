---
title: What is the method for determining if a variable is present?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a variable exists in Python by using the `in` operator.
---

**Contents**

[TOC]

# Check if Variable Exists

## Option 1: `in` Operator 
The `in` operator can be used to check if a variable is present in a given sequence. For example, to check if a variable `x` exists in a list `my_list`, we can use the following syntax: 

```python
if x in my_list:
    # do something
```

## Option 2: `hasattr()` Function
The `hasattr()` function can be used to check if an object has a given attribute. For example, to check if a variable `x` exists in an object `my_obj`, we can use the following syntax: 

```python
if hasattr(my_obj, x):
    # do something
```

## Option 3: `getattr()` Function
The `getattr()` function can be used to check if an object has a given attribute and return the value of the attribute. For example, to check if a variable `x` exists in an object `my_obj`, we can use the following syntax: 

```python
if getattr(my_obj, x, None) is not None:
    # do something
```

## Option 4: `locals()` and `globals()`
The `locals()` and `globals()` functions can be used to check if a variable exists in the local or global scope, respectively. For example, to check if a variable `x` exists in the global scope, we can use the following syntax: 

```python
if x in globals():
    # do something
```
