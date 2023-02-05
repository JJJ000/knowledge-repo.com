---
title: What is the procedure for determining if a key is present in a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `in` operator to check if a key exists in a dictionary in Python.
---

**Contents**

[TOC]

# Using the `in` Keyword

The `in` keyword can be used to check if a key exists in a dictionary. It will return `True` if the key exists in the dictionary and `False` if it does not.

```python
d = {'name': 'John', 'age': 24}

# Check if key 'name' exists
print('name' in d)
# Output: True

# Check if key 'job' exists
print('job' in d)
# Output: False
```

# Using the `get()` Method

The `get()` method can be used to check if a key exists in a dictionary. It will return the value of the key if it exists in the dictionary and `None` if it does not.

```python
d = {'name': 'John', 'age': 24}

# Check if key 'name' exists
print(d.get('name'))
# Output: John

# Check if key 'job' exists
print(d.get('job'))
# Output: None
```

# Using the `dict.keys()` Method

The `dict.keys()` method can be used to check if a key exists in a dictionary. It will return a list of all the keys in the dictionary.

```python
d = {'name': 'John', 'age': 24}

# Check if key 'name' exists
print('name' in d.keys())
# Output: True

# Check if key 'job' exists
print('job' in d.keys())
# Output: False
```

# Using the `dict.items()` Method

The `dict.items()` method can be used to check if a key exists in a dictionary. It will return a list of tuples containing the key-value pairs in the dictionary.

```python
d = {'name': 'John', 'age': 24}

# Check if key 'name' exists
print('name' in dict(d.items()))
# Output: True

# Check if key 'job' exists
print('job' in dict(d.items()))
# Output: False
```
