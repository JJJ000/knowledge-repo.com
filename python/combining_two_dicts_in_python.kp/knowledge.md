---
title: What is the most pythonic method for merging two dictionaries and adding the values for any shared keys?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, you can use the {**dict1, **dict2} syntax to combine two dicts, adding values for keys that appear in both.
---

**Contents**

[TOC]

**1. Using the `update()` Method:**

The `update()` method can be used to combine two dicts in a pythonic way. It adds the key-value pairs of one dict to the other, overwriting any existing keys.

Example:
```python
dict1 = {'a':1, 'b':2}
dict2 = {'b':3, 'c':4}

dict1.update(dict2)

print(dict1)
# Output: {'a':1, 'b':3, 'c':4}
```

**2. Using the `ChainMap` Class:**

The `ChainMap` class from the `collections` module can also be used to combine two dicts. It creates a list of dicts and searches through them in order. This allows the same key to appear in multiple dicts, with the value from the first dict being used.

Example:
```python
from collections import ChainMap

dict1 = {'a':1, 'b':2}
dict2 = {'b':3, 'c':4}

chain = ChainMap(dict1, dict2)

print(chain)
# Output: ChainMap({'a': 1, 'b': 2}, {'b': 3, 'c': 4})
```

**3. Using the `dict()` Constructor:**

The `dict()` constructor can also be used to combine two dicts. It takes a list of tuples and creates a dict from them. This allows the same key to appear multiple times, with the value from the last tuple being used.

Example:
```python
dict1 = {'a':1, 'b':2}
dict2 = {'b':3, 'c':4}

combined_dict = dict(list(dict1.items()) + list(dict2.items()))

print(combined_dict)
# Output: {'a':1, 'b':3, 'c':4}
```

**4. Using the `{**dict1, **dict2}` Syntax:**

Python 3.5 introduced the `{**dict1, **dict2}` syntax for combining dicts. This syntax takes the key-value pairs from both dicts and combines them into a new dict. Any duplicate keys will be overwritten with the value from the second dict.

Example:
```python
dict1 = {'a':1, 'b':2}
dict2 = {'b':3, 'c':4}

combined_dict = {**dict1, **dict2}

print(combined_dict)
# Output: {'a':1, 'b':3, 'c':4}
```
