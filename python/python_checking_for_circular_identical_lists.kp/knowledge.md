---
title: What is the process for verifying if two lists are identical in a circular manner using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: One way to check whether two lists are circularly identical in Python is to concatenate one list to itself and see if the other list is a contiguous subsequence of the concatenated list.
---

**Contents**

[TOC]

## Define circularly identical lists in Python

To say that two lists are circularly identical means that they have the same elements in the same order, even if one of them has been rotated.

For example, `[1,2,3,4]` and `[4,1,2,3]` are circularly identical lists.

Let's create two lists called `list1` and `list2` to test whether they are circularly identical.

```python
list1 = [1, 2, 3, 4]
list2 = [4, 1, 2, 3]
```

## Method 1: Check if one list is a rotation of the other

One way of checking if two lists are circularly identical is to check if one of them is a rotation of the other.

We can do this by concatenating one of the lists to itself and checking if the other list is a sublist of the concatenated list.

```python
def is_circularly_identical(list1, list2):
    if len(list1) != len(list2):
        return False
    return ''.join(map(str, list2)) in ''.join(map(str, list1*2))

print(is_circularly_identical(list1, list2)) # True
```

## Method 2: Check if both lists have the same elements

Another way of checking if two lists are circularly identical is to check if they have the same elements, regardless of their position in the list.

We can do this by checking if both lists have the same length and contain the same elements.

```python
def is_circularly_identical(list1, list2):
    if len(list1) != len(list2):
        return False
    return set(list1) == set(list2)

print(is_circularly_identical(list1, list2)) # True
```

## Method 3: Check if both lists have the same order after rotation

A third way of checking if two lists are circularly identical is to check if they have the same order of elements after one of them has been rotated.

We can do this by rotating one of the lists until we find a match.

```python
def is_circularly_identical(list1, list2):
    if len(list1) != len(list2):
        return False
    for i in range(len(list2)):
        if list1 == list2[i:]+list2[:i]:
            return True
    return False

print(is_circularly_identical(list1, list2)) # True
```

All the above methods can be used to determine if two lists are circularly identical in Python.
