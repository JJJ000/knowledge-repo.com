---
title: Valueerror it is not possible to determine the truth value of an array that contains more than one element. please use either the a.any() or a.all() function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use a.any() or a.all() to check the truth value of an array with more than one element.
---

**Contents**

[TOC]

# Solution

## Using a.all()

The `a.all()` method returns `True` if all elements of the given iterable are `True`, otherwise it returns `False`. For example, if we have an array `a = [True, True, False]`, then `a.all()` will return `False`.

## Using a.any()

The `a.any()` method returns `True` if any of the elements of the given iterable is `True`, otherwise it returns `False`. For example, if we have an array `a = [True, False, False]`, then `a.any()` will return `True`.

## When to use a.all() or a.any()

When dealing with an array with more than one element, it is important to consider which method to use. If we want to check if all elements in the array are `True`, then we should use the `a.all()` method. If we want to check if any of the elements in the array is `True`, then we should use the `a.any()` method.
