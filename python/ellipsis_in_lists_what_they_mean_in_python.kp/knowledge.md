---
title: What is the meaning of ellipsis [...] when used in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Ellipsis [...] is used as a placeholder to represent a sequence of items in a list or an array in Python.
---

**Contents**

[TOC]

1. Introduction: 
In Python, ellipsis is a special object that represents an omission or missing value in a list. It is denoted by a set of three consecutive dots "..." and is often used in conjunction with slicing operations.

2. Slicing with Ellipsis:
One common use of ellipsis in lists is for slicing operations. When used in a slice notation, ellipsis can be used to represent any number of indices in a list. For instance, given a list of shape (3,4,5), we can use ellipsis to slice along two dimensions like myList[1, ..., 4]. The ellipsis tells Python to take all indices between the second and fourth dimensions, including endpoints.

3. Using Ellipsis in Function Arguments:
Another use of ellipsis in Python is as a placeholder argument in function definitions that take variable-length arguments. When a function definition includes the ellipsis symbol as a parameter, it is known as a variadic argument. This allows the function to take any number of arguments, and they will all be passed in as a tuple. For example, def func(*args, ...) will take any number of arguments and represent them as a tuple args.

4. Conclusion:
In summary, ellipsis in Python is used to represent missing values or omitted values in a list or array. It can be used for slicing operations and as a placeholder for variable-length function arguments. Mastering ellipsis is essential for Python developers who work with lists or arrays regularly.
