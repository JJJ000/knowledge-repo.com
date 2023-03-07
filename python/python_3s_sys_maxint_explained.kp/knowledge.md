---
title: Can you explain what sys.maxint denotes in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python 3, `sys.maxint` has been removed and the maximum value of integers is now limited only by available memory.
---

**Contents**

[TOC]

Introduction 
Python3 represents an infinite integer as an object of "int" type. You don't have to worry about the capacity of integers when operating with big integers in Python. 

sys.maxint in Python 3
The sys.maxint constant was required in Python 2 to represent the largest positive integer that can be stored within an "int" object. However, in Python 3, "int" objects have no fixed limit, and allocating the maximum value permitted by available physical memory is possible. As a result, the sys.maxint constant is no longer available, having been removed from Python 3.

Alternative ways to resolve this issue.
However, in certain circumstances, your application may need to determine the maximum value of an integer type that can be represented on the operating system that it is running on. If this is the case, the sys.maxsize attribute may be used, which returns the upper bound of the size of integers that can be processed in Python. 

Conclusion
sys.maxint is an obsolete constant in Python3, since Python3 automatically handles arbitrary length integers. Instead, use the sys.maxsize attribute to get the maximum representable integer in Python3.
