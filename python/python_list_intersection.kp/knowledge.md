---
title: Determine whether there are any shared elements between lists in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Check if any item in list 1 is also in list 2 using the intersection operator (“&”).
---

**Contents**

[TOC]

## Introduction
In Python, it is often necessary to check whether two or more lists have shared items or elements. In this article, we will discuss some of the ways to test whether lists share any items in Python.

## Method 1: Using Set Intersection
One straightforward way to check whether two or more lists have shared items is to use the set intersection method. This method involves converting each list into a set and then computing the intersection of the sets. If the intersection of the sets is not empty, then it implies that the two lists share at least one item. Here is an example:

``` python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
list3 = [9, 10, 11, 12, 13]

set1 = set(list1)
set2 = set(list2)
set3 = set(list3)

# Check if list1 and list2 have shared items
if set1.intersection(set2):
    print("list1 and list2 have shared items")
else:
    print("list1 and list2 do not have shared items")

# Check if list2 and list3 have shared items
if set2.intersection(set3):
    print("list2 and list3 have shared items")
else:
    print("list2 and list3 do not have shared items")
```

Output:
```python
list1 and list2 have shared items
list2 and list3 do not have shared items
```

## Method 2: Using Looping
Another way to test whether two or more lists have shared items is to use loops. We can loop through each item in one list and check whether it occurs in another list. If there is at least one common item, then the two lists have shared items. Here is an example:

```python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
list3 = [9, 10, 11, 12, 13]

# Check if list1 and list2 have shared items
for item in list1:
    if item in list2:
        print("list1 and list2 have shared items")
        break    # Exit the loop once a shared item is found

# Check if list2 and list3 have shared items
for item in list2:
    if item in list3:
        print("list2 and list3 have shared items")
        break    # Exit the loop once a shared item is found
```

Output:
```python
list1 and list2 have shared items
```

## Method 3: Using the `any()` Function
Another alternative is to use the `any()` function in Python. This function returns `True` if at least one item in the iterable is true, and `False` otherwise. We can pass a generator expression that checks whether each item in the first list is in the second list. Here is an example:

``` python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
list3 = [9, 10, 11, 12, 13]

# Check if list1 and list2 have shared items
if any(item in list2 for item in list1):
    print("list1 and list2 have shared items")
else:
    print("list1 and list2 do not have shared items")

# Check if list2 and list3 have shared items
if any(item in list3 for item in list2):
    print("list2 and list3 have shared items")
else:
    print("list2 and list3 do not have shared items")
```

Output:
``` python
list1 and list2 have shared items
list2 and list3 do not have shared items
```

## Conclusion
In this article, we discussed three different ways to test whether two or more lists have shared items in Python. These methods include using set intersection, loops, and the `any()` function. Other methods, such as using list comprehension or the `set()` function, can also be used for this purpose.
