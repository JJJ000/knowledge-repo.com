---
title: What is the best way to maintain the original order of keys and values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using an OrderedDict from the collections module can ensure that keys and values remain in the same order as declared.
---

**Contents**

[TOC]

# Using OrderedDict

OrderedDict is a subclass of the built-in dict class that remembers the order in which its contents are added. It can be used to store and retrieve key-value pairs in the same order as they are declared.

## Creating an OrderedDict

An OrderedDict can be created in the following way:

```python
from collections import OrderedDict

d = OrderedDict()
d['a'] = 1
d['b'] = 2
d['c'] = 3
```

## Adding Elements

Elements can be added to an OrderedDict using the `update()` method:

```python
d.update({'d': 4})
```

## Accessing Elements

The elements of an OrderedDict can be accessed in the same order as they were declared. For example:

```python
for key, value in d.items():
    print(key, value)

# Output:
# a 1
# b 2
# c 3
# d 4
```
