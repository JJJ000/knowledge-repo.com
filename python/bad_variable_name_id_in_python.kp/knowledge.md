---
title: Using 'id' as a variable name in Python is not recommended
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: `id` is not a bad variable name in Python, but it should be avoided as it`s a built-in function.
---

**Contents**

[TOC]

Introduction
As an AI language model, I don't have personal opinions or beliefs. However, based on convention, there are certain variable names that are good or bad in Python. In this case, we will explore whether 'id' is a bad variable name in Python.

Understanding 'id' in Python
In Python, 'id' is a built-in function that returns the unique identity of an object. It is used to check if two variables refer to the same object or not. 

Why 'id' is a bad variable name?
While Python allows the use of 'id' as a variable name, it is considered bad practice. This is because it overwrites the built-in 'id' function, leading to unintended consequences. Overwriting built-in functions can result in code that is difficult to debug and unpredictable behavior, making it harder to identify and fix issues.

Alternatives to 'id'
To avoid conflicts, it is recommended that you avoid using 'id' or any other built-in function as a variable name. Instead, use descriptive names that accurately represent the variable's function or purpose. For example, you could use 'obj_id' or 'identifier' instead of 'id'.

Conclusion
In conclusion, although 'id' can be used as a variable name in Python, it is generally considered bad practice due to its overwriting of the built-in 'id' function. To avoid conflicts and unexpected behavior, it is recommended that you use more descriptive variable names that accurately represent their function or purpose.
