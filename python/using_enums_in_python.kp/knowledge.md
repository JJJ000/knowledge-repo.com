---
title: What is the best way to create an 'enum' in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: An `Enum` can be represented in Python as an instance of the `Enum` class.
---

**Contents**

[TOC]

#1 Creating an Enum in Python
Python does not have native support for Enums, but the Python Enum library provides the functionality to create them. To create an Enum in Python, the Enum class is imported from the library and then used to create the Enum object. The Enum object is then populated with the desired values, which can be either strings or integers.

#2 Accessing Enum Values
Once an Enum has been created, it can be accessed by calling the Enum object and passing in the desired value. The Enum object will then return the associated value.

#3 Iterating Over Enums
Enums can also be iterated over using the built-in Python iter() function. This allows for easy access to all the values in the Enum without having to manually access each one.

#4 Comparing Enums
Enums can also be compared using the == operator. This allows for easy comparison of two Enums to see if they are equal or not.
