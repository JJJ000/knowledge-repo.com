---
title: What is the best way to make a copy of a list so that it does not get modified after it has been assigned?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To clone a list so that it doesn't change unexpectedly after assignment, use the `list()` or `copy.deepcopy()` functions.
---

**Contents**

[TOC]

### Understanding Cloning
Cloning is the process of creating a copy of a data structure. This is useful when you want to make changes to a copy of a data structure without affecting the original. Cloning a list in Python is possible using the list() constructor or the slicing operator.

### Using the list() Constructor
The list() constructor can be used to create a new list with the same values as the original list. The syntax for this is as follows:

```python
new_list = list(original_list)
```

This will create a new list with the same values as the original list.

### Using the Slicing Operator
The slicing operator can also be used to create a new list with the same values as the original list. The syntax for this is as follows:

```python
new_list = original_list[:]
```

This will create a new list with the same values as the original list.

### Conclusion
Cloning a list in Python is possible using the list() constructor or the slicing operator. This is useful when you want to make changes to a copy of a data structure without affecting the original.
