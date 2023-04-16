---
title: What is the process for finding the cartesian product of multiple lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `itertools.product()` function to get the cartesian product of a series of lists in Python.
---

**Contents**

[TOC]

# Section 1: Understanding Cartesian Product

A Cartesian product is the result of multiplying two or more sets of elements together. It is also known as a cross product and is denoted by the symbol X. The Cartesian product of two sets A and B, denoted by A X B, is the set of all ordered pairs (a, b) where a is an element of A and b is an element of B.

# Section 2: Using itertools.product()

Python’s itertools module provides a function called product() which can be used to calculate the Cartesian product of a series of lists. The product() function takes an iterable of iterables as its argument and returns an iterator over the Cartesian product of the elements of the input iterables.

# Section 3: Example

Let’s take an example to understand how to use the product() function. Consider the following lists:

list1 = [1, 2, 3] 
list2 = [4, 5, 6] 
list3 = [7, 8, 9]

To get the Cartesian product of these three lists, we can use the following code:

from itertools import product 

cartesian_product = list(product(list1, list2, list3)) 
print(cartesian_product)

The output of the above code will be:

[(1, 4, 7), (1, 4, 8), (1, 4, 9), (1, 5, 7), (1, 5, 8), (1, 5, 9), (1, 6, 7), (1, 6, 8), (1, 6, 9), (2, 4, 7), (2, 4, 8), (2, 4, 9), (2, 5, 7), (2, 5, 8), (2, 5, 9), (2, 6, 7), (2, 6, 8), (2, 6, 9), (3, 4, 7), (3, 4, 8), (3, 4, 9), (3, 5, 7), (3, 5, 8), (3, 5, 9), (3, 6, 7), (3, 6, 8), (3, 6, 9)]

# Section 4: Conclusion

In this article, we have seen how to calculate the Cartesian product of a series of lists using the product() function from the itertools module. We have also seen an example to understand the usage of the product() function better.
