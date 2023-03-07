---
title: Combining dictionary objects in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The union of dict objects in Python can be achieved using the update() method.
---

**Contents**

[TOC]

# 1. Introduction

In Python, a dictionary is a collection of key-value pairs. Sometimes we need to merge or combine two or more dictionaries into a single dictionary. This is useful when we have multiple dictionaries with overlapping or complementary data, and we want to create a unified view of that data. One way to do this is to use the union operator.

# 2. Union operator

The union operator is represented by two vertical bars (`|`). When applied to two dictionaries, it returns a new dictionary that contains all the key-value pairs from both dictionaries. If there are keys that are common to both dictionaries, the value from the second dictionary is used.

Here's an example:

```python
dict1 = {'a': 1, 'b': 2}
dict2 = {'b': 3, 'c': 4}

merged_dict = dict1 | dict2

print(merged_dict)  # {'a': 1, 'b': 3, 'c': 4}
```

In this example, the `merged_dict` contains all the key-value pairs from both `dict1` and `dict2`. The value for the key `'b'` is `3`, which comes from `dict2`.

# 3. Union with multiple dictionaries

The union operator can also be used to merge more than two dictionaries. Here's an example:

```python
dict1 = {'a': 1, 'b': 2}
dict2 = {'b': 3, 'c': 4}
dict3 = {'d': 5}

merged_dict = dict1 | dict2 | dict3

print(merged_dict)  # {'a': 1, 'b': 3, 'c': 4, 'd': 5}
```

In this example, we merge three dictionaries using the union operator. The resulting dictionary contains all the key-value pairs from all three dictionaries.

# 4. Conclusion

The union operator is a simple and efficient way to merge two or more dictionaries into a single dictionary. It's particularly useful when we have multiple dictionaries with overlapping or complementary data, and we want to create a unified view of that data.
