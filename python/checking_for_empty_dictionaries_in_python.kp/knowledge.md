---
title: What is the method for determining if a dictionary is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To check if a dictionary is empty in Python, use the boolean expression `not dict` or `len(dict) == 0`.
---

**Contents**

[TOC]

# Method 1

Using the `len()` Function

The `len()` function can be used to determine whether a dictionary is empty. The `len()` function returns the number of items in the dictionary, which is 0 if the dictionary is empty.

```python
my_dict = {}

if len(my_dict) == 0:
    print("The dictionary is empty")
```

# Method 2

Using the `bool()` Function

The `bool()` function can also be used to determine whether a dictionary is empty. The `bool()` function returns `False` if the dictionary is empty.

```python
my_dict = {}

if not bool(my_dict):
    print("The dictionary is empty")
```

# Method 3

Using the `in` Operator

The `in` operator can be used to determine whether a dictionary is empty. The `in` operator returns `False` if the dictionary is empty.

```python
my_dict = {}

if not any(my_dict):
    print("The dictionary is empty")
```

# Method 4

Using the `not` Operator

The `not` operator can also be used to determine whether a dictionary is empty. The `not` operator returns `True` if the dictionary is empty.

```python
my_dict = {}

if not my_dict:
    print("The dictionary is empty")
```
