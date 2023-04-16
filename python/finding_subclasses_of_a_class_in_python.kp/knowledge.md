---
title: What is the process for locating all the subclasses of a particular class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in `\_\_subclasses\_\_` method on the class object to find all subclasses of a class given its name in Python.
---

**Contents**

[TOC]

##### Section 1: Using the `inspect` Module

The `inspect` module in Python provides several useful functions to help you find the subclasses of a class. To find all the subclasses of a given class, you can use the `getclasstree` function. This function takes a class as an argument and returns a list of all the subclasses of that class.

##### Section 2: Using the `__subclasses__` Method

Another way to find all the subclasses of a class is to use the `__subclasses__` method. This method returns a list of all the subclasses of the class. However, it only returns the direct subclasses and not the subclasses of the subclasses.

##### Section 3: Using the `class_hierarchy` Function

The `class_hierarchy` function in the `inspect` module can be used to find all the subclasses of a class. This function takes a class as an argument and returns a list of all the subclasses, including the subclasses of the subclasses.

##### Section 4: Using the `isinstance` Function

The `isinstance` function can also be used to find all the subclasses of a class. This function takes two arguments: an instance of the class and the class itself. It then returns `True` if the instance is an instance of the class or one of its subclasses, and `False` otherwise. By iterating through all the instances of the class and testing them with the `isinstance` function, you can find all the subclasses of the class.
