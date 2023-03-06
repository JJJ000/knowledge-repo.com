---
title: What are the steps to make a deep copy of a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use slicing to create a new list with all the elements of the original list `new\_list = original\_list[]`.
---

**Contents**

[TOC]

## Introduction

In Python, copying a list is not as simple as just assigning it to a new variable. One needs to perform a deep copy operation to create a completely separate copy of the original list. This tutorial will walk through several methods for performing a deep copy of a list in Python.

## Using the copy() method

The simplest way to deep copy a list in Python is to use the built-in `copy()` method. This method creates a new object with the same values as the original list.

```python
list1 = [1, 2, 3, [4, 5]]
list2 = list1.copy()

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # [1, 2, 3, [4, 5]]

# modify list2
list2[0] = 'one'
list2[3][0] = 'four'

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # ['one', 2, 3, ['four', 5]]
```

## Using the deepcopy() method

The `deepcopy()` method from the `copy` module is an alternate way to deep copy a list. This method creates a new object with the same values as the original list, but it also recursively copies any nested lists, dictionaries, or other mutable objects.

```python
import copy

list1 = [1, 2, 3, [4, 5]]
list2 = copy.deepcopy(list1)

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # [1, 2, 3, [4, 5]]

# modify list2
list2[0] = 'one'
list2[3][0] = 'four'

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # ['one', 2, 3, ['four', 5]]
```

## Using slicing

Another way to perform a deep copy of a list is to use slicing. This method creates a new object with the same values as the original list.

```python
list1 = [1, 2, 3, [4, 5]]
list2 = list1[:]

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # [1, 2, 3, [4, 5]]

# modify list2
list2[0] = 'one'
list2[3][0] = 'four'

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # ['one', 2, 3, ['four', 5]]
```

## Using list comprehension

Finally, list comprehension can be used to perform a deep copy of a list. This is more of a shortcut than a recommended method.

```python
list1 = [1, 2, 3, [4, 5]]
list2 = [item for item in list1]

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # [1, 2, 3, [4, 5]]

# modify list2
list2[0] = 'one'
list2[3][0] = 'four'

print(list1)    # [1, 2, 3, [4, 5]]
print(list2)    # ['one', 2, 3, ['four', 5]]
```

## Conclusion

In Python, there are several ways to deep copy a list. The built-in `copy()` method and the `deepcopy()` method from the `copy` module are the recommended ways to perform a deep copy. Slicing and list comprehension are less recommended, but still effective methods.
