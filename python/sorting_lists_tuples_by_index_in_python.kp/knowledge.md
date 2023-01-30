---
title: What is the best way to organize a list/tuple of lists/tuples based on the value of a specific element?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `sorted` function, passing in the list/tuple and a key parameter that references the element at the given index.
---

**Contents**

[TOC]

# Section 1: Understanding the Problem

When sorting a list/tuple of lists/tuples by the element at a given index, we are looking to rearrange the elements in the list/tuple according to the value of the element at the specified index. For example, if we have a list of tuples such as `[(5, 2), (1, 4), (3, 6)]` and we want to sort this list by the element at index 0, the result would be `[(1, 4), (3, 6), (5, 2)]`. 

# Section 2: Using the `sorted()` Method

The simplest way to sort a list/tuple of lists/tuples by the element at a given index is to use the built-in `sorted()` method. The `sorted()` method takes an iterable as an argument and returns a sorted list. We can also specify an optional `key` parameter which is used to specify a function to be called on each list element prior to making comparisons. 

For example, if we have the list of tuples `[(5, 2), (1, 4), (3, 6)]` and we want to sort this list by the element at index 0, we could use the following code:

```python
sorted([(5, 2), (1, 4), (3, 6)], key=lambda x: x[0])
```

The `lambda x: x[0]` expression is a lambda function that takes an element `x` and returns the element at index 0. This allows us to sort the list by the element at index 0.

# Section 3: Using the `operator.itemgetter()` Method

Another way to sort a list/tuple of lists/tuples by the element at a given index is to use the `operator.itemgetter()` method. The `operator.itemgetter()` method takes an index as an argument and returns a callable which can be used as the `key` parameter for the `sorted()` method. 

For example, if we have the list of tuples `[(5, 2), (1, 4), (3, 6)]` and we want to sort this list by the element at index 0, we could use the following code:

```python
import operator
sorted([(5, 2), (1, 4), (3, 6)], key=operator.itemgetter(0))
```

# Section 4: Using the `sort()` Method

The third way to sort a list/tuple of lists/tuples by the element at a given index is to use the built-in `sort()` method. The `sort()` method takes an optional `key` parameter which is used to specify a function to be called on each list element prior to making comparisons. 

For example, if we have the list of tuples `[(5, 2), (1, 4), (3, 6)]` and we want to sort this list by the element at index 0, we could use the following code:

```python
list = [(5, 2), (1, 4), (3, 6)]
list.sort(key=lambda x: x[0])
```

The `lambda x: x[0]` expression is a lambda function that takes an element `x` and returns the element at index 0. This allows us to sort the list by the element at index 0.
