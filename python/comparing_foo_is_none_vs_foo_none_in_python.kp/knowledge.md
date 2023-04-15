---
title: Do "foo is none" and "foo == none" have any dissimilarity?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: No, both expressions are equivalent and check if the object referenced by `foo` is None in Python.
---

**Contents**

[TOC]

Introduction
------------
In Python, when dealing with variables that can have a value or be empty, we often check if they are empty using the None keyword. However, there are two ways to check if a variable is None - using 'is' and '==' operators. This article examines whether there is a difference between the two.

Identity operator: "is"
------------------------
In Python, "is" is the identity operator that checks whether two variables refer to the same object. Therefore, "foo is None" checks whether the "foo" variable refers to the None object. If the "foo" variable refers to the None object, the expression returns True, otherwise, False. 

Comparison operator: "=="
---------------------------
On the other hand, "foo == None" is the equality operator that checks whether the value of the "foo" variable is equal to the value of the None object. If the "foo" variable is equal to None, the expression returns True, otherwise, False. 

Conclusion
----------
In summary, there is no practical difference between "foo is None" and "foo == None" expressions. They both check whether the variable "foo" is None. However, using "is" is more efficient and faster than using "==" since it checks identity rather than value equality. Therefore, it is recommended to use "foo is None" when checking for None in Python.
