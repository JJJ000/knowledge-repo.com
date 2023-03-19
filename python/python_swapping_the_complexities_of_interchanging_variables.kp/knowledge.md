---
title: What is the reason for the difference between b, a = b, a and a, b = a, b in terms of Python swapping?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The order in which the assignments occur matters, since the right-hand side of the assignment is evaluated first before being assigned to the left-hand side.
---

**Contents**

[TOC]

Introduction
Python is a versatile language that allows programmers to perform several operations, such as swapping values. Swapping values is an essential programming technique that is used to interchange the values stored in two variables. In Python, swapping is achieved using the assignment operator (=) with either a temporary variable, a tuple packing and unpacking, or a simultaneous exchange method using only one line of code. One such method is the technique of writing a, b = b, a. However, this method is sometimes buggy and may not work as intended. This article aims to explore why a, b = b, a is not always equivalent to b, a = a, b.

Tuple Packing and Unpacking 
In Python, multiple values can be assigned to several variables by separating them with commas. The resulting group of values is called a tuple, and it is written within parentheses. Similarly, multiple variables can be unpacked to receive different values by separating them with commas. In the context of swapping two variables, tuple packing and unpacking can be a straightforward method that eliminates the need for a temporary variable. When executed, the operation involves putting the two variables' values into a tuple, unpacking the tuple, and assigning its values to the two variables. For instance, consider swapping the values in x and y:

    x = 10
    y = 15
    x, y = y, x

The values of x and y will be swapped, and the output will be as follows:

    >>> print(x)
    15
    >>> print(y)
    10

Possible Issues with a, b = b, a Method 
Although the a, b = b, a technique can be used to swap variables, it is not always equivalent to b, a = a, b. This method works by creating a temporary tuple containing the two variables' values and then assigning them to the new variables. However, if one or both variables are mutable objects, such as lists or dictionaries, the a, b = b, a method won't work correctly. This issue arises because mutable objects are stored by reference and not by value. Therefore, when the a, b = b, a method is used, the new variables will hold the same reference to the same objects, rather than copies of them. For example:

    a = [1, 2]
    b = [3, 4]
    a, b = b, a

Executing this code will swap the variables a and b, but the result will be unexpected. Instead of containing their original values, the variables a and b will reference the same objects as each other. 

The Correct Way to Swap Mutable Objects 
To correctly swap variables that may contain mutable objects, a different swapping mechanism must be used. One such method is to create a shallow copy of each object before the swap. A shallow copy creates a new object with the same content as the original object, but its internal references point to the same objects as the original. By performing a shallow copy of the objects, the internal references can be broken, and they can be correctly swapped. For example:

    a = [1, 2]
    b = [3, 4]
    a[:], b[:] = b, a

This code will swap the variables a and b, and each variable will contain a shallow copy of the original object.

Conclusion 
Swapping variables in Python can be achieved using tuple packing and unpacking, a temporary variable, or a simultaneous swapping method using a single line of code. However, the method of a, b = b, a is not always equivalent to b, a = a, b. This method may work when the variables contain immutable objects, but it won't work when mutable objects are involved. To correctly swap mutable objects, a shallow copy of the objects must be created before the objects are swapped. By creating a shallow copy of the objects, the objects' internal references will be broken, and they can be safely swapped.
