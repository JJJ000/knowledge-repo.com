---
title: What is the way to deal with exceptions while using list comprehensions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the try-except statement inside the list comprehension to handle exceptions.
---

**Contents**

[TOC]

Section 1: Introduction
Exceptions are run-time errors that occur while a program is executing. These errors can occur due to various reasons, such as an invalid input or an unexpected behavior of the program. Python provides a way to handle these exceptions through the 'try-except' block. However, when it comes to list comprehensions, the syntax for handling exceptions is slightly different. In this tutorial, we will learn how to handle exceptions in list comprehensions in Python.

Section 2: Syntax
The syntax to handle exceptions in list comprehensions is as follows:

```
[expression for item in list if condition]
```

When an exception occurs in the expression part of the list comprehension, the entire list comprehension is stopped, and the exception is raised. To handle this exception, we can use the 'try-except' block inside the expression part of the list comprehension. The modified syntax would look like this:

```
[try_expression if try_block else except_expression for item in list if condition]
```

In this syntax, the 'try_expression' is the expression that will be evaluated, and the 'try_block' is the block of code that might raise an exception. The 'except_expression' is the expression that will be used if the exception occurs in the 'try_block'. 

Section 3: Example
Let's take an example to illustrate this concept:

Suppose we have a list of integers, and we want to create a new list that contains the square root of each integer in the original list. However, if an integer is negative, we want to replace it with zero in the new list.

We can use a list comprehension to achieve this:

```
import math

original_list = [1, 2, 3, -4, 5, 6, -7, 8, 9]

new_list = [math.sqrt(item) if item > 0 else 0 for item in original_list]

print(new_list)
```

Output:
```
[1.0, 1.4142135623730951, 1.7320508075688772, 0, 2.23606797749979, 2.449489742783178, 0, 2.8284271247461903, 3.0]
```

In this example, we have used the 'if' statement in the list comprehension to check if the item is greater than zero. If it is, we evaluate the square root of the item using the 'math.sqrt()' function. Otherwise, we replace it with zero.

Section 4: Conclusion
In this tutorial, we have learned how to handle exceptions in list comprehensions in Python. We have discussed the syntax for handling exceptions in list comprehensions and provided an example to illustrate this concept. With this knowledge, we can write list comprehensions that are robust and handle any exceptions that may occur during their execution.
