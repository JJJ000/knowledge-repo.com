---
title: Do the keys() and values() of a Python dictionary always appear in the same order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, the order of keys() and values() in a Python dictionary is not always the same.
---

**Contents**

[TOC]

# Yes 
Dictionaries in Python are unordered collections, meaning that the order in which the keys and values are stored can change over time. However, the keys() and values() methods always return the same order. 

# How it Works
The keys() and values() methods both return a view object, which is an object that provides a dynamic view of the dictionary’s data. The view object stores the keys and values in the same order, so when the view is iterated, the same order is always returned. 

# Examples
For example, if a dictionary is created like this:

```
d = {'a':1, 'b':2, 'c':3}
```

The keys() and values() methods will return the same order:

```
>>> d.keys()
dict_keys(['a', 'b', 'c'])
>>> d.values()
dict_values([1, 2, 3])
```

# Summary
In summary, the keys() and values() methods in Python dictionaries always return the same order. This is because they both return a view object, which stores the keys and values in the same order.
