---
title: How to check if a given key already exists in a dictionary in Python? 
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-06 00:00:00
updated_at: 2023-01-06 00:00:00
tldr: You can use the `in` keyword to check if a given key exists in a dictionary in Python.
---

**Contents**

[TOC]

### Using 'in' Operator

The easiest way to check if a given key already exists in a dictionary is to use the 'in' operator. The 'in' operator returns a boolean value (True or False) depending on whether the specified key is present in the dictionary or not.

Syntax:
```python
key in dictionary
```

Example:
```python
d = {'name': 'John', 'age': 20}

print('name' in d)  # Output: True

print('gender' in d)  # Output: False
```

### Using dict.keys()

The dict.keys() method returns a view object that contains the keys of the dictionary. We can use this view object to check if a given key is present in the dictionary or not.

Syntax:
```Python
key in dict.keys()
```

Example:
```Python
d = {'name': 'John', 'age': 20}

print('name' in d.keys())  # Output: True

print('gender' in d.keys())  # Output: False
```

### Using dict.get()

The dict.get() method returns the value of the specified key from the dictionary. We can use this method to check if a given key is present in the dictionary or not.

Syntax:
```Python
dict.get(key)
```

Example:
```Python
d = {'name': 'John', 'age': 20}

print(d.get('name'))  # Output: John

print(d.get('gender'))  # Output: None
```
