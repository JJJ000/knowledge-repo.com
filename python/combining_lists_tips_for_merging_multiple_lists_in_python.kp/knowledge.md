---
title: What is the process of combining several lists into a single list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the + operator to concatenate the lists into one list.
---

**Contents**

[TOC]

# Introduction
Python provides various ways to merge multiple lists into a single list. In this tutorial, we will discuss some of the ways to merge lists in Python.

# Method 1: Using the + operator
One of the simplest methods to merge lists is by using the + operator. The +  operator concatenates the two lists into a new list.  
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]
merged_list = list1 + list2
print(merged_list)
```
Output: [1, 2, 3, 4, 5, 6]

# Method 2: Using the extend() method
The extend() method adds elements from the iterable to the end of the list. Here, we can extend the first list with the elements from the second list.
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]
list1.extend(list2)
print(list1)
```
Output: [1, 2, 3, 4, 5, 6]

# Method 3: Using list comprehension
List comprehension can also be used as an alternative method to merge two lists.
```
list1 = [1, 2, 3]
list2 = [4, 5, 6]
merged_list = [i for i in list1+list2]
print(merged_list)
```
Output: [1, 2, 3, 4, 5, 6]

# Conclusion
In this tutorial, we covered three methods to merge multiple lists into a single list in Python. You can use any of the methods as per your need and convenience.
