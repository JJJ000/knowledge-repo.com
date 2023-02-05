---
title: What are the new type annotation features in Python 3.5?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Type hints in Python 3.5 are annotations that allow for type checking of function parameters and return values.
---

**Contents**

[TOC]

# What are Type Hints?
Type hints are a way of providing additional type information about the values of variables to the interpreter. They are used to help the interpreter better understand the code and provide more accurate type information.

# How Do Type Hints Work?
Type hints are added to the source code of a Python program by using the typing module. The typing module provides a set of type hints that can be used to annotate the variables in a program. When the program is compiled, the type hints are used to generate type information that is used by the interpreter to better understand the code.

# Benefits of Type Hints
Using type hints can help make code more readable and maintainable by making it easier to understand the types of values that are being used. It can also help improve performance by allowing the interpreter to better optimize code.

# Limitations of Type Hints
Type hints are not a replacement for type checking, and they are not enforced by the interpreter. This means that it is possible for code to be written that does not adhere to the type hints. Additionally, type hints can only be used with Python 3.5 and higher.
