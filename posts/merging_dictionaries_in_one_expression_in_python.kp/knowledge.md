---
title: How do I merge two dictionaries in one expression?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can merge two dictionaries in a single expression by using the `{**dict1, **dict2}` syntax.
---

**Contents**

[TOC]

### Syntax
The syntax to merge two dictionaries in a single expression in Python is:

`{**dict1, **dict2}`

### Example
The following example shows how to merge two dictionaries in a single expression in Python:

```python
dict1 = {'a': 1, 'b': 2}
dict2 = {'c': 3, 'd': 4}

dict_merged = {**dict1, **dict2}

print(dict_merged)
# Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}
```

### How it Works
The `{**dict1, **dict2}` syntax works by unpacking the contents of the two dictionaries and combining them into a single dictionary. The `**` operator is used to unpack the contents of the dictionaries and the resulting dictionary contains all the keys and values from both dictionaries.
