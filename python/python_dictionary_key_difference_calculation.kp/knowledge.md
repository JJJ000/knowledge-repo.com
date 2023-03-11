---
title: Determine the disparity of the keys that exist in two Python dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To calculate the difference in keys contained in two Python dictionaries, we can use set operations and find the symmetric difference between their keys set.
---

**Contents**

[TOC]

# Steps to calculating the difference in keys contained in two Python dictionaries

1. Initialize two dictionaries: 

```python
dict1 = {'a': 1, 'b': 2, 'c': 3}
dict2 = {'b': 4, 'd': 5, 'e': 6}
```

2. Convert the keys of each dictionary to a set:

```python
set1 = set(dict1.keys())
set2 = set(dict2.keys())
```

3. Find the difference between the two sets:

```python
diff = set1.difference(set2)
```

4. Print the difference:

```python
print(diff)
```

The result should show `{'a', 'c'}` which are the keys that are in `dict1` but not in `dict2`. 

# Explanation

The first step is to initialize two dictionaries that we want to compare. In this case, we have two dictionaries `dict1` and `dict2`.

The second step is to convert the keys of each dictionary to a set. This is done because we want to find the difference between the keys of the two dictionaries. 

The third step is to find the difference between the two sets. In Python, we can use the `difference()` method to find the difference between two sets.

Finally, we print the difference between the two dictionaries as the result. The result should show the keys that are in `dict1` but not in `dict2`, which are `{'a', 'c'}`.
