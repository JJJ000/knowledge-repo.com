---
title: Could you explain the message conveyed by pylint's "too few public methods"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Pylint`s `Too few public methods` message means that a class has fewer than the minimum recommended number of public methods.
---

**Contents**

[TOC]

### Overview

When using Pylint for Python code analysis, one of the messages you might encounter is "Too few public methods". This message indicates that the class being analyzed has too few public methods defined in it.

### The Meaning of "Public Methods"

In Python, a method is considered to be public if it's defined with no leading underscore in its name. Public methods are intended to be accessed and used by other parts of the software that use the class. On the other hand, methods that start with an underscore (e.g., `_private_method()`) are considered to be private, and are intended to be used only within the class itself.

### Why This Message Matters

The "Too few public methods" message in Pylint matters because it indicates that the class may not be designed to be used correctly by other parts of the software. If a class has too few public methods, it may be difficult for other developers to use it effectively, or at all. Conversely, if a class has too many public methods, it may be difficult to maintain, and may violate principles of good object-oriented programming design.

### What to Do About It

If you receive the "Too few public methods" message when running Pylint on your Python code, it's a good idea to review the class structure and determine whether more public methods are needed to make the class more usable by other parts of the software. However, it's important to be cautious not to add too many public methods, as this can make the class more complex and difficult to maintain over time. Following best practices for object-oriented programming can help to strike the right balance.
