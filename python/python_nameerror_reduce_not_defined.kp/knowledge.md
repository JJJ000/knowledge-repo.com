---
title: The name 'reduce' is not defined in python, resulting in a nameerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The reduce function is part of the functools module, and needs to be imported before being used in code.
---

**Contents**

[TOC]

Section 1: Explanation of the Error

The "NameError: 'reduce' is not defined" error is raised by Python when it cannot find a built-in function called "reduce". This error typically occurs when the "reduce" function is not imported from the "functools" module or not defined in the current scope.

Section 2: Understanding the reduce() Function

The "reduce()" function is a built-in function in Python that allows us to apply a function to a sequence of values and reduce them to a single output value. It takes two arguments: a function and an iterable. The function is applied to the first two elements of the iterable, and then the result is used with the next element of the iterable until we end up with a single output value.

Section 3: Solving the Error

If you encounter this error, you need to import the "reduce" function from the "functools" module. You can do this by adding the following line at the beginning of your code:

from functools import reduce

This will import the "reduce" function, and you will be able to use it in your code.

Section 4: Example Code

Here's an example code that demonstrates the use of the "reduce" function:

from functools import reduce

lst = [1, 2, 3, 4, 5] # list of numbers to be reduced
sum = reduce(lambda a, b: a + b, lst) # apply the sum function to the list

print(sum) # prints 15 (1 + 2 + 3 + 4 + 5)
