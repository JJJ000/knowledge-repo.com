---
title: What is the reason that a function can change certain arguments from the perspective of the caller while leaving others unaltered?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Arguments that are mutable objects can be modified by the function and will be perceived by the caller, while immutable objects cannot be modified by the function and will not be perceived by the caller.
---

**Contents**

[TOC]

# Pass by Object Reference

Python is a pass-by-object-reference language which means that objects are not directly passed to a function. Instead, the function is given a reference (memory address) to the object, and any modifications that occur to the object within the function change the original object.

# Mutable vs Immutable Objects

Mutable objects can be modified in place, while immutable objects cannot. Examples of mutable objects are lists and dictionaries, while strings and tuples are immutable.

# Modifying Objects in a Function

When an argument is passed to a function, the function creates a local reference to the original object. Therefore, if the original object is mutable, the function can modify the object in place.

However, if the original object is immutable, the function cannot modify it. Instead, the function creates a new object with the modifications and returns it. This is how some functions can appear to modify their arguments, while others cannot. 

In conclusion, functions can modify some arguments as perceived by the caller when they are mutable objects. Immutable objects cannot be modified in place, but the function can return a new object with the modifications.
