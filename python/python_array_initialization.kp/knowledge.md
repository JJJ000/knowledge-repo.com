---
title: Creating a fixed-size array in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python, an array of fixed size can be initialized using the array module by specifying the data type and the size of the array.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, arrays can be initialised in multiple ways depending on the requirement of the program. One way to initialise an array is by specifying its size in advance. In this case, the array will have a fixed size, and the size cannot be changed during runtime. This method of initialisation is useful in cases where the size of the array is known in advance and is not expected to change.

Section 2: Using a list comprehension
One way to initialise an array of fixed size in Python is by using a list comprehension. For example, to create an array of length n filled with zeros, we can use the following code:
```python
n = 5
arr = [0 for i in range(n)]
```
This creates a list of size n, with all elements initialised to 0. We can access the elements of the list by using the index position.

Section 3: Using a for loop
Another way to initialise an array of a fixed size in Python is to use a for loop. For example, to create an array of length n filled with ones, we can use the following code:
```python
n = 5
arr = [None] * n
for i in range(n):
    arr[i] = 1
```
In this approach, we start by creating a list of length n, with all elements initialised to None. We then use a for loop to set each element of the list to the desired value.

Section 4: Conclusion
Initialising an array of fixed size in Python can be done using either a list comprehension or a for loop. The choice of approach depends on the programmer's preference and the requirements of the program. Regardless of the method used, it is essential to ensure that the array is of the desired size and that all elements are initialised correctly.
