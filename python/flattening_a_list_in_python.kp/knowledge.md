---
title: Converting a shallow list into a single list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Using a list comprehension, it is possible to flatten a shallow list in Python by combining all the sub-lists into one list.
---

**Contents**

[TOC]

### Using List Comprehension

List comprehension is a concise way to create a list from an existing list. It is a powerful tool that can be used to flatten a shallow list. To flatten a shallow list using list comprehension, the following syntax can be used:

```python
flattened_list = [item for sublist in list for item in sublist]
```

### Using the itertools Module

The itertools module can also be used to flatten a shallow list. The syntax for using the itertools module is as follows:

```python
import itertools
flattened_list = list(itertools.chain.from_iterable(list))
```

### Using a For Loop

A for loop can also be used to flatten a shallow list. The syntax for using a for loop is as follows:

```python
flattened_list = []
for sublist in list:
    for item in sublist:
        flattened_list.append(item)
```

### Using the Reduce Function

The reduce function can also be used to flatten a shallow list. The syntax for using the reduce function is as follows:

```python
from functools import reduce
flattened_list = reduce(lambda x,y: x+y, list)
```
