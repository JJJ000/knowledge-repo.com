---
title: What is the implementation of set()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: set() in Python is implemented using hash table data structure which allows constant time operations like add, remove and lookup.
---

**Contents**

[TOC]

## Overview

In Python, `set()` is a built-in function used to create a set object, a mutable collection of unique and hashable elements. Whenever an iterable is passed to `set()`, it returns a new set object containing all unique elements in the iterable. In this article, we'll explore how `set()` is implemented in Python, including its algorithms and data structures.

## Hash Tables

Hash tables are the primary data structure used in implementing `set()`. A hash table is a collection of key-value pairs that uses a hash function to determine the index or slot where the value will be stored in an array. The hash function takes the value to be stored and returns an integer, which is used as the index.

In Python, the built-in `hash()` function is used to generate hash codes for values. The hash code is used as the index in the hash table, allowing for very fast access to elements in the set.

## Time Complexity

The time complexity of the `set()` function depends on the size of the iterable passed to it. If the iterable has n elements, the time complexity of constructing the set will be O(n). This is because each element needs to be added to the hash table, which has a constant time complexity of O(1) on average. However, if there are collisions in the hash table, the time complexity can become O(n log n) or even O(n^2) in the worst case.

## Conclusion

In conclusion, `set()` is implemented in Python using hash tables, which allow for constant-time access to elements in the set. The time complexity of creating a set is O(n) on average, but can become O(n log n) or O(n^2) in the worst case. Overall, `set()` is a very useful and efficient function in Python for creating collections of unique elements.
