---
title: Could you explain how Python performs comparison of tuples?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Tuple comparison in Python compares the elements of each tuple in order, and stops at the first difference it encounters, returning the result of the comparison of the corresponding elements.
---

**Contents**

[TOC]

## Introduction 

Tuple comparison is a process of comparing two tuples to determine whether they are equal or not based on their respective elements. In Python, it is possible to compare tuples using the standard comparison operators such as `==`, `<=` and `>=`. The comparison of tuples is performed element-wise, and it is based on the types of the elements, their order, and the values stored within them.

## Element-wise Comparison 

Python compares tuples element-wise, and this means that each element stored within the tuple is compared with the corresponding element of the other tuple. For instance, if you have two tuples (1, 2, 3) and (4, 5, 6), the first element of the first tuple will be compared with the first element of the second tuple. This operation continues until all elements of both tuples are compared.

## Value Comparison 

During the element-wise comparison, Python checks whether the values of both elements are the same. If they are the same, they are considered equal. If the values are not equal, Python will compare them based on their values. For instance, if you have two tuples, A=(1,2,3) and B=(1,2,4), Python will compare A[0] and B[0], A[1] and B[1], and so on.

## Ordering Comparison 

If the values of the elements are the same, Python will compare the order of the elements within each tuple. This means that if you have two tuples (1, 2, 3) and (1, 3, 2), Python will return false since the order of the elements within both tuples is different.

## Conclusion 

In conclusion, Tuple comparison in Python is performed element-wise, and it is based on the types of the elements, their order, and the values stored within them. Python compares tuples values based on their order and type, and if the values are the same, Python compares the order of the elements within each tuple, and the output is returned based on the comparison results.
