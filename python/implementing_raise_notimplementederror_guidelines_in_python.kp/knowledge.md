---
title: In what situations is it appropriate to use 'raise notimplementederror'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To demonstrate that a method has not been implemented in a class and should be overridden by the child class.
---

**Contents**

[TOC]

Use of raise NotImplementedError in Python

`raise NotImplementedError` is a type of exception that comes in handy when using Python, and it's often necessary to determine how to use it in various sections of a Python project.

1. Definition
The primary function of `raise NotImplementedError` is to indicate that a specific function's implementation is not done yet. When a function is still under development and not ready to be executed, this exception is thrown.

2. Implementation
This code is frequently utilized in abstract base classes, which may help check whether their implementation is comprehensive. This is an instance when a developer creates a "template" for a class but does not add any details to them.

3. Functionality
When a line of code containing a `raise NotImplementedError` statement is run, the interpreter will stop executing and raise an exception stating that the feature is not yet functional, preventing errors from propagating further in the program.

4. Best Practice
It is essential to mention that raising a `NotImplementedError` is not the same as raising a plain old `NotImplemented` exception. The latter is often utilized as a return value that informs a caller that a certain function is not capable of executing a specific operation, while a return `NotImplementedError` exception informs the caller that the function is not implemented.
