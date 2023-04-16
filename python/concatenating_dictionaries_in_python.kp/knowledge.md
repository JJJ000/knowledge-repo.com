---
title: What is the process for combining two dictionaries to form a new one?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To concatenate two dictionaries in Python, use the update() method to add the contents of one dictionary to another.
---

**Contents**

[TOC]

# Section 1: Creating the New Dictionary

The easiest way to concatenate two dictionaries to create a new one is to use the `update()` method. This method adds the elements of one dictionary to another dictionary.

Example:

```
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

dict1.update(dict2)

print(dict1)
```

Output: `{'a': 1, 'b': 2, 'c': 3, 'd': 4}`

# Section 2: Merging Dictionaries

Another way to concatenate two dictionaries is to use the `dict()` constructor. This method takes in an iterable object like a list of tuples and creates a new dictionary object.

Example:

```
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

dict3 = dict(list(dict1.items()) + list(dict2.items()))

print(dict3)
```

Output: `{'a': 1, 'b': 2, 'c': 3, 'd': 4}`

# Section 3: Using ChainMap

The `ChainMap` class from the `collections` module can also be used to concatenate two dictionaries. This class takes in multiple dictionaries and creates a single view of all the dictionaries.

Example:

```
from collections import ChainMap

dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

dict3 = ChainMap(dict1, dict2)

print(dict3)
```

Output: `ChainMap({'a': 1, 'b': 2}, {'c': 3, 'd': 4})`

# Section 4: Using the `**` Operator

The `**` operator can also be used to concatenate two dictionaries. This operator takes in two dictionaries and creates a new dictionary with the combined elements from both the dictionaries.

Example:

```
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

dict3 = {**dict1, **dict2}

print(dict3)
```

Output: `{'a': 1, 'b': 2, 'c': 3, 'd': 4}`
