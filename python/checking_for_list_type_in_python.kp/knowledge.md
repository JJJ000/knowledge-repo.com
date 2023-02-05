---
title: Verifying if the data type is a list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, you can use the `type` function to check if an object is a list in Python.
---

**Contents**

[TOC]

# Answer

## Using the `type()` Function
Python's `type()` function can be used to check the type of a given object. To check if an object is a list, the following code can be used:

```python
if type(object) == list:
    # Do something
```

## Using the `isinstance()` Function
The `isinstance()` function can also be used to check the type of an object. To check if an object is a list, the following code can be used:

```python
if isinstance(object, list):
    # Do something
```

## Using the `in` Operator
The `in` operator can be used to check if an object is a member of a given type. To check if an object is a list, the following code can be used:

```python
if list in object:
    # Do something
```

## Using the `is` Operator
The `is` operator can also be used to check if an object is a member of a given type. To check if an object is a list, the following code can be used:

```python
if object is list:
    # Do something
```
