---
title: Can you explain the distinctions among normal assignment operation, shallow copy, and deep copy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Shallow copy creates a new object which stores a reference to the original object, while deepcopy creates a new object with a new memory address, and normal assignment operation creates a reference to the original object.
---

**Contents**

[TOC]

## Introduction

In Python, data is stored in objects that are assigned to variables. When copying or reassigning variables, there are several ways to do it, and the behavior of each method can be different, depending on the type of data stored in the object. This article will explore the differences between shallow copy, deepcopy, and normal assignment operations in Python.

## Normal assignment operation

Normal assignment operation is the simplest way to copy or reassign variables in Python. When a variable is assigned a new value, it simply points to the memory location where the new data is stored. This means that the original object is not duplicated, and any changes made to the new variable will also affect the original object. This behavior is usually desired when working with immutable objects like integers, strings, or tuples.

```python
a = 1
b = a     # normal assignment
b = 2     # reassign b
print(a)  # Output: 1
print(b)  # Output: 2
```

In the example above, the variable `b` is assigned to the value of `a`, which is integer `1`. After that, `b` is reassigned with the value `2`, without changing `a`. The output shows that `a` is still equal to `1`, while `b` is now `2`.

## Shallow copy

A shallow copy creates a new object that is a copy of the original object, but the copy only contains references to the original data. In other words, the original object is not duplicated, and any changes made to the new object will affect the original object. Shallow copy is useful when working with mutable objects like lists or dictionaries, but it can lead to unexpected results if not used properly.

```python
a = [1, 2, [3, 4]]
b = a.copy()  # shallow copy
b[0] = 5
b[2][0] = 6
print(a)  # Output: [1, 2, [6, 4]]
print(b)  # Output: [5, 2, [6, 4]]
```

In the example above, the variable `b` is assigned a shallow copy of the list stored in `a`. Both `a` and `b` point to the same list object, but their memory locations are different. After that, the elements `0` of `b` and `2, 0` of `b` are modified. The output shows that both `a` and `b` are affected by the changes.

## Deepcopy

Deepcopy creates a completely new object that is a copy of the original object, including all sub-objects. This means that any changes made to the new object will not affect the original object. Deepcopy is useful when working with complex or nested data structures, but it can be slow and memory-intensive.

```python
import copy

a = [1, 2, [3, 4]]
b = copy.deepcopy(a)
b[0] = 5
b[2][0] = 6
print(a)  # Output: [1, 2, [3, 4]]
print(b)  # Output: [5, 2, [6, 4]]
```

In the example above, the method `deepcopy()` from the `copy` module is used to create a completely new object for `b`. The original object `a` is not affected by the changes made to `b`, as shown by the output.
