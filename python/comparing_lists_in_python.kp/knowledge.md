---
title: What is the method to confirm if two Python lists hold identical elements?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Check if the sorted versions of the two lists are equal.
---

**Contents**

[TOC]

## 1. Using Python Sets

One common approach to assert if two lists contain the same elements is by converting the lists to sets and comparing them. Sets are unordered collections of unique elements, hence converting the lists to sets and comparing them will eliminate duplicates and ignore order. Here's how to do it:

```python
list1 = [1, 2, 3]
list2 = [3, 1, 2]

if set(list1) == set(list2):
    print("The lists contain the same elements.")
else:
    print("The lists do not contain the same elements.")
```

## 2. Using Python Counter

Another approach is to use Python's Counter module. A Counter is a dictionary subclass that counts the occurrences of elements in a collection. Here's how to use it to assert if two lists have the same elements:

```python
from collections import Counter

list1 = [1, 2, 3]
list2 = [3, 1, 2]

if Counter(list1) == Counter(list2):
    print("The lists contain the same elements.")
else:
    print("The lists do not contain the same elements.")
```

## 3. Using Python Sorting

Another way to assert if two lists contain the same elements is to sort the lists and compare them. Here's how to do that:

```python
list1 = [1, 2, 3]
list2 = [3, 1, 2]

list1.sort()
list2.sort()

if list1 == list2:
    print("The lists contain the same elements.")
else:
    print("The lists do not contain the same elements.")
```

## 4. Using Set Intersection

Finally, we can also use set intersection to assert if two lists contain the same elements. Here's how to do it:

```python
list1 = [1, 2, 3]
list2 = [3, 1, 2]

if set(list1).intersection(list2) == set(list1):
    print("The lists contain the same elements.")
else:
    print("The lists do not contain the same elements.")
```

All of these methods will return True if the two lists contain the same elements, regardless of the order they appear in.
