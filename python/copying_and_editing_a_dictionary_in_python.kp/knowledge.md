---
title: How to make a duplicate of a dictionary and only make changes to the duplicate
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To make a copy of a dictionary and edit the copy, use the dict.copy() method.
---

**Contents**

[TOC]

# Section 1: Creating a Copy

There are two main ways to create a copy of a dictionary in Python:

1. Using the `dict.copy()` method: 
```
original_dict = {'a': 1, 'b': 2}
copied_dict = original_dict.copy()
```

2. Using the `dict()` constructor: 
```
original_dict = {'a': 1, 'b': 2}
copied_dict = dict(original_dict)
```

# Section 2: Editing the Copy

Once you have created a copy of the dictionary, you can edit the copied dictionary without affecting the original dictionary. For example, you can add a new key-value pair, remove an existing key-value pair, or modify the value of an existing key-value pair.

# Section 3: Examples

Adding a new key-value pair:
```
copied_dict['c'] = 3
```

Removing an existing key-value pair:
```
del copied_dict['b']
```

Modifying the value of an existing key-value pair:
```
copied_dict['a'] = 4
```

# Section 4: Verifying the Changes

To verify that the changes made to the copied dictionary did not affect the original dictionary, you can print both dictionaries and compare the results.

For example:
```
print('Original Dictionary: ', original_dict)
print('Copied Dictionary: ', copied_dict)
```

This will output:

```
Original Dictionary:  {'a': 1, 'b': 2}
Copied Dictionary:  {'a': 4, 'c': 3}
```
