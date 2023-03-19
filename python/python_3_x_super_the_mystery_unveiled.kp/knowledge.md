---
title: What makes super() function magical in Python 3.x?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python 3.x`s super() is magic because it allows for easier and more flexible inheritance and method overriding.
---

**Contents**

[TOC]

# Introduction
`super()` is a built-in function in Python 3.x that provides a powerful and flexible way to access and manipulate the parent class of a subclass. It is widely considered to be one of the most useful and powerful features of the language, and is often referred to as "magic" due to its ability to simplify and streamline the process of inheritance in Python.

# The Basics of super()
At its most basic level, `super()` allows a subclass to access and call methods, properties, and other attributes of its parent class. This makes it much easier to create complex class hierarchies and to reuse code between classes, as it eliminates the need to manually define or rewrite the same code in multiple places.

# The Flexibility of super()
One of the key benefits of `super()` is its flexibility. Unlike other inheritance mechanisms in Python, `super()` allows subclasses to access their parent class in a dynamic, runtime-based way. This means that the parent class can be changed or modified at runtime, and the subclass will still be able to access and call the correct methods and attributes.

# The Advantages of super()
Overall, `super()` is widely regarded as a highly useful and powerful feature of Python, as it simplifies and streamlines the process of inheritance and allows developers to create complex class hierarchies with relative ease. By providing a flexible and dynamic way to access and manipulate parent classes, `super()` helps to make Python code more modular, reusable, and maintainable.
