---
title: Is there a mutable named tuple in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, Python has a built-in data type called `namedtuple` that can be mutable when defined with the `mutable` argument.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, a named tuple is a subclass of a tuple that has named fields. A named tuple is immutable, which means once it is created, its values cannot be changed. However, there are situations where it might be useful to have a mutable named tuple. This article will explore whether a mutable named tuple exists in Python.

Section 2: What is a Mutable Named Tuple?
A mutable named tuple is a named tuple whose values can be changed after it is created. In Python, tuples are immutable, which makes it impossible to change the values of a named tuple after it is created. However, a mutable named tuple would allow the values to be changed.

Section 3: Is a Mutable Named Tuple Possible in Python?
No, a mutable named tuple is not possible in Python. A named tuple is a subclass of a tuple, and tuples are immutable. Once a tuple is created, its values cannot be changed. This means that a named tuple, whether named or not, cannot be made mutable.

Section 4: Alternatives to a Mutable Named Tuple
While a mutable named tuple is not possible in Python, there are alternatives that can be used instead. One option is to use a class with properties. A class can have attributes that can be set and changed after the object is created. This is similar to using a named tuple, but with the added benefit of being mutable.

Another option is to use a dictionary to store the values. A dictionary can be easily changed by adding, removing, or updating key-value pairs. This approach does not provide the structure that a named tuple would, but it allows for mutation.

Overall, while a mutable named tuple is not possible in Python, there are alternatives that can be used in situations where mutability is needed.
