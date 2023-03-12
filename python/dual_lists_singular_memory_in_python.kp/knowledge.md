---
title: What is the reason for similar lists having distinct memory footprints?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The memory footprint of two identical lists can differ if they are stored in different locations in memory.
---

**Contents**

[TOC]

## Introduction

Python is an interpreted, high-level, general-purpose programming language used for various purposes such as scripting, web development, machine learning, scientific computing, and more. Python provides various built-in data structures that help in storing and manipulating data efficiently. Two such data structures are lists and tuples. In this article, we will explore why two identical lists have different memory footprints in Python.

## Memory Management in Python

Python uses a dynamic memory management technique called Automatic Memory Management or Garbage Collection. The Garbage Collector reclaims memory that is no longer being used by the program. Python allocates memory to an object only when the object is created. The size of this allocated memory depends on the type of the object and the data it holds.

## Lists in Python

Lists are one of the built-in data structures in Python. Lists are mutable, ordered, and can have multiple data types. Lists allocate memory based on the data types of the elements they hold. For example, if a list has integers, it allocates memory based on the size of an integer. If a list has strings, it allocates memory based on the size of a string. Lists can grow or shrink dynamically based on the number of elements they hold.

## Why Two Identical Lists have Different Memory Footprints

Two identical lists can have different memory footprints because Python treats them as two different objects in memory. Even though the two lists have the same values, they might have different identities or addresses in memory. When we create a new list in Python, the Python interpreter locates a block of memory that is large enough to hold the size of the list object. The location of this block of memory is recorded as the identity of the list. If we create another identical list, Python allocates a different block of memory to hold the new list object. This new block of memory has a different identity than the first list. Therefore, two identical lists have different memory footprints because they have different identities, even though they have the same values.

## Conclusion

In conclusion, two identical lists can have a different memory footprint in Python because Python treats them as two different objects in memory. The identity or address of an object in Python is used to track its position in memory. When we create two identical objects, Python treats them as separate objects and allocates different blocks of memory to hold them. This results in different memory footprints for the two identical lists. It's important to keep this in mind while writing Python programs that deal with multiple objects, so as not to mistakenly assume that two identical objects have the same memory footprint.
