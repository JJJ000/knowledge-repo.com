---
title: What is the procedure for determining if a specific value is present in a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `in` operator to check if a value exists in a dictionary in Python.
---

**Contents**

[TOC]

# Option 1: Using 'in' Operator

The `in` operator can be used to check if a value exists in a dictionary. It returns a Boolean value of `True` if the value exists in the dictionary, and `False` if it does not.

Example: 

```python
dictionary = {
    'name': 'John',
    'age': 25
}

if 'name' in dictionary:
    print("Name exists in dictionary")
```

# Option 2: Using 'get()' Method

The `get()` method can also be used to check if a value exists in a dictionary. It returns the value if it exists in the dictionary, and `None` if it does not.

Example: 

```python
dictionary = {
    'name': 'John',
    'age': 25
}

if dictionary.get('name') is not None:
    print("Name exists in dictionary")
```
