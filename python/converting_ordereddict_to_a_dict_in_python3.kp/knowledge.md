---
title: What is the method to change an ordereddict to a standard dict in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can simply use the built-in dict() function to convert an OrderedDict to a regular dict in Python3.
---

**Contents**

[TOC]

# 1. Introduction
An OrderedDict is a subclass in the collections module that keeps the order of keys in which they were inserted. It is a dictionary-like object that has extra capabilities of maintaining the order. The built-in `dict()` function can be used to convert an OrderedDict to a regular dictionary in python 3.

# 2. Using the `dict()` function
The easiest way to convert an OrderedDict into a regular dict in python is by using the in-built `dict()` function. Here's how,

```python
from collections import OrderedDict

ordered_dict = OrderedDict([('a', 1), ('b', 2), ('c', 3)])
regular_dict = dict(ordered_dict)
```

# 3. Using a loop
Another way to convert an OrderedDict to a regular dictionary is to use a loop to iterate over the key-value pairs in the OrderedDict and add them one by one to a new regular dictionary. Here's how,

```python
from collections import OrderedDict

ordered_dict = OrderedDict([('a', 1), ('b', 2), ('c', 3)])

regular_dict = {}
for key, value in ordered_dict.items():
    regular_dict[key] = value
```

# 4. Using the `json` module
The `json` module in python can also be used to convert an OrderedDict into a regular dictionary. Here's how,

```python
import json
from collections import OrderedDict

ordered_dict = OrderedDict([('a', 1), ('b', 2), ('c', 3)])

json_string = json.dumps(ordered_dict)
regular_dict = json.loads(json_string)
```
