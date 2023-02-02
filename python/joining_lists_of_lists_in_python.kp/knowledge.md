---
title: Combine multiple lists into one list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `sum` function to join a list of lists in Python.
---

**Contents**

[TOC]

# Solution 1: Using the + Operator

The `+` operator can be used to join two or more lists together.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list1 + list2 # [1, 2, 3, 4, 5, 6]
```

# Solution 2: Using the extend() Method

The `extend()` method can be used to add all the elements of one list to another list.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list1.extend(list2) # [1, 2, 3, 4, 5, 6]
```

# Solution 3: Using the itertools.chain() Method

The `itertools.chain()` method can be used to join multiple iterables together.

```python
import itertools

list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = list(itertools.chain(list1, list2)) # [1, 2, 3, 4, 5, 6]
```

# Solution 4: Using the sum() Method

The `sum()` method can be used to join multiple lists together.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

list3 = sum([list1, list2], []) # [1, 2, 3, 4, 5, 6]
```
