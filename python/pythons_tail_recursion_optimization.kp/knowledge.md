---
title: Is tail recursion optimization supported by python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: No, Python does not optimize tail recursion.
---

**Contents**

[TOC]

Introduction
------------

Tail recursion is a type of recursion where the function calls itself as the last operation before it returns. This type of recursion has an optimization called tail recursion optimization, which optimizes the recursive calls so that they don't consume extra memory. In this article, we will discuss whether Python optimizes tail recursion or not.

Tail Recursion Optimization
---------------------------

Tail recursion optimization is an optimization technique that eliminates recursive calls from functions when the recursion is in the tail position. To be in the tail position, the recursive call must be the last operation of the function. When the optimization is applied, the recursive call is replaced with a loop, which makes the function run faster and consume less memory.

Python and Tail Recursion
-------------------------

Python does not optimize tail recursion by default. This means that if you write a tail-recursive function in Python, it will consume more memory than a non-tail-recursive function. However, Python provides a module called `sys` that can be used to increase the recursion limit. By increasing the recursion limit, you can write tail-recursive functions that can be used in practice.

Limitations of Tail Recursion Optimization in Python
----------------------------------------------------

While increasing the recursion limit can be useful in some cases, it is not a perfect solution. Tail recursion optimization in Python is limited by the call stack size. When the call stack is full, the program will crash with a `RecursionError`. This means that tail-recursive functions must be used with caution in Python, particularly if you are dealing with large datasets or complex algorithms.

Conclusion
----------

In conclusion, Python does not optimize tail recursion by default. However, the `sys` module can be used to increase the recursion limit, allowing you to write tail-recursive functions that can be used in practice. Nevertheless, tail recursion optimization in Python is limited by the call stack size, which can cause your program to crash if the recursion limit is exceeded. As a result, tail-recursive functions should be used with caution in Python.
