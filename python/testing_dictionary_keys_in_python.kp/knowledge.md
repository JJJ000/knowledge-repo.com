---
title: What is the procedure for determining if a dictionary has a particular key?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the in operator to test if a dictionary contains a specific key.
---

**Contents**

[TOC]

# Using the "in" Operator

The `in` operator can be used to test if a key exists in a dictionary. It returns a boolean value of `True` if the key is present and `False` if not.

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}

# Test if 'name' is a key in my_dict

if 'name' in my_dict:
    print('Name is a key in the dictionary.')
```

# Using the "get()" Method

The `get()` method can also be used to test if a key exists in a dictionary. It returns the value of the key if it exists and `None` if the key is not present.

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}

# Test if 'name' is a key in my_dict

if my_dict.get('name') is not None:
    print('Name is a key in the dictionary.')
```

# Using the "try/except" Block

The `try/except` block can be used to test if a key exists in a dictionary. It allows you to try to access the key and catch the `KeyError` exception if the key is not present.

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}

# Test if 'name' is a key in my_dict

try:
    my_dict['name']
    print('Name is a key in the dictionary.')
except KeyError:
    print('Name is not a key in the dictionary.')
```
