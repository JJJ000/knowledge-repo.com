---
title: What is the reason for a Python dict.update() not to give back the object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Because it updates the dictionary in place and does not create a new object.
---

**Contents**

[TOC]

## 1. background 

Python is an open source, interpreted, high-level, general-purpose programming language. It supports different data structures, including lists, tuples, sets, and dictionaries. One of the key features of Python is its ability to manipulate dictionaries in various ways, including updating existing ones.

The `dict.update()` method is used to update a dictionary with a new or another dictionary. It takes as an argument, another dictionary, and updates the calling dictionary by adding the key-value pairs of the argument dictionary to it. 

## 2. dictionary mutability

In Python, dictionaries are mutable objects. This means that they can be modified after they are created. Modifications include adding or removing elements, updating key-value pairs, or changing the order of elements. 

The `dict.update()` method is one such method that modifies a dictionary. It updates the calling dictionary in place. As a result, the dictionary that the method is called upon is modified.

## 3. the return value

Although the `dict.update()` method modifies the calling dictionary in place, it does not return any value. Instead, it returns `None`. This is because the method modifies the calling dictionary directly without creating a new dictionary or returning any other value. 

This behavior is consistent with other Python methods that perform modifications in place, such as the `list.sort()` method, which sorts a list in place without returning a value. 

## 4. conclusion

In conclusion, the `dict.update()` method modifies the calling dictionary directly without returning a value. This behavior is consistent with other Python methods that perform modifications in place. Since Python dictionaries are mutable objects, the `dict.update()` method is a useful feature in programming.
