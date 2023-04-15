---
title: Reworded "if a" versus "if a has a value that is not none"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Both conditions check whether variable A has a value assigned to it, but `if A is not None` is more explicit and considered to be a more Pythonic way of checking for a None value.
---

**Contents**

[TOC]

Introduction:
In Python, logical conditionals are used to check if a given condition is True or False. Two common ways of checking if a variable or value exists are using the `if A` and `if A is not None` statements. In this article, we will discuss how these two statements differ and when to use each one.

Section 1: The `if A` Statement
The `if A` statement checks if the variable or expression A is True. In Python, several values evaluate to False, including empty lists, dictionaries, and strings, as well as zero, None, and False. Therefore, `if A` will be False when A is any of these values, and True for any other value. 

Section 2: The `if A is not None` Statement
The `if A is not None` statement checks if the variable A is not None. In Python, None is a special value that represents the absence of a value. Therefore, `if A is not None` will be True if A has any value other than None, and False if A is None.

Section 3: Differences between `if A` and `if A is not None`
The main difference between `if A` and `if A is not None` is that the former checks if A is True, while the latter checks if A is not None. Therefore, `if A is not None` will be True for any value of A other than None, whether or not it evaluates to True. On the other hand, `if A` will be True for any value of A that evaluates to True, including None.

Section 4: When to use `if A` vs `if A is not None`
Use `if A` when you want to check if A evaluates to True or False, regardless of whether it is None or not. For example, if you want to check if a list is not empty, you can use `if my_list`. Use `if A is not None` when you specifically want to check if A is not None, regardless of whether it evaluates to True or False. For example, if you want to check if a variable has been assigned a value, you can use `if my_var is not None`. 

Conclusion:
In summary, the `if A` statement checks if A evaluates to True or False, while the `if A is not None` statement checks if A is not None. You should use `if A` when you want to check if A is True or False and `if A is not None` when you specifically want to check if A is not None, regardless of its truth value.
