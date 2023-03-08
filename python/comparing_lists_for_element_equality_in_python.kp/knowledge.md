---
title: Can you identify whether two lists contain identical elements, regardless of their arrangement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `set` function and compare the sets to see if they are equal, as sets are unordered collections of unique elements.
---

**Contents**

[TOC]

Approach 1: Sorting and Comparison

One way to determine if 2 lists have the same elements, regardless of order, is to sort the lists and compare them element-wise. Here's how you could implement this approach:

```python
def same_elements(list1, list2):
    sorted1 = sorted(list1)
    sorted2 = sorted(list2)
    return sorted1 == sorted2
```

This function takes in two lists (list1 and list2), sorts them using Python's built-in `sorted()` function, and then compares the two sorted lists using the `==` operator. If the two lists have the same elements (regardless of order), then the function will return `True`. Otherwise, it will return `False`.

Note that this approach has a time complexity of O(n log n), where n is the length of the input lists, due to the sorting step.

Approach 2: Counting and Comparison

Another way to determine if 2 lists have the same elements, regardless of order, is to count the occurrences of each element in each list and compare the resulting counts. Here's how you could implement this approach:

```python
def same_elements(list1, list2):
    count1 = {elem: list1.count(elem) for elem in set(list1)}
    count2 = {elem: list2.count(elem) for elem in set(list2)}
    return count1 == count2
```

This function takes in two lists (list1 and list2), uses the `set()` function to get a set of unique elements in each list, and then uses a dictionary comprehension to count the occurrences of each unique element in each list. It then compares the resulting count dictionaries using the `==` operator. If the two lists have the same elements (regardless of order), then the function will return `True`. Otherwise, it will return `False`.

Note that this approach has a time complexity of O(n), where n is the length of the input lists, due to the counting step.

Approach 3: Set Comparison

A third way to determine if 2 lists have the same elements, regardless of order, is to convert the lists to sets and compare the resulting sets. Here's how you could implement this approach:

```python
def same_elements(list1, list2):
    set1 = set(list1)
    set2 = set(list2)
    return set1 == set2
```

This function takes in two lists (list1 and list2), converts them to sets using Python's built-in `set()` function, and then compares the resulting sets using the `==` operator. If the two lists have the same elements (regardless of order), then the function will return `True`. Otherwise, it will return `False`.

Note that this approach has a time complexity of O(n), where n is the length of the input lists, due to the set conversion step. However, this approach may not preserve the order of the elements in the original lists if that is important.
