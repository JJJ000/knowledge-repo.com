---
title: What makes "if none.__eq__("a")" appear to be true (though not entirely)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Because `None` is not equal to any object, but does not raise an error when compared to any object using the `==` operator.
---

**Contents**

[TOC]

Section 1: Understanding the `__eq__()` Method
The `__eq__()` method is a special method used in Python for object comparison. It checks if two object instances are equal and returns True if they are and False otherwise. 

Section 2: None Comparison in Python
In Python, `None` is an object that represents the absence of a value. When we compare `None` to another object using the `==` operator or the `__eq__()` method, it always returns False unless the second object is also `None`. 

Section 3: Evaluating `None.__eq__("a")`
In the expression `None.__eq__("a")`, we are calling the `__eq__()` method of the `None` object with "a" as the argument. Normally, this should return False since we cannot compare `None` with a string.

Section 4: Why does `if None.__eq__("a")` seem to evaluate to True (but not quite) in Python?
However, in Python, the `__eq__()` method of `None` is implemented differently from other objects. It returns True only if the other object is also `None`. This is a special case implemented to simplify code and prevent errors by ensuring that `None` is always compared only with `None`. Therefore, `None.__eq__("a")` actually returns False, but when we use it in an `if` statement, it evaluates to True because anything other than `None` is considered True in Python.
