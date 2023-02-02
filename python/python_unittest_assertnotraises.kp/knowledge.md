---
title: Assertnotraises
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The opposite of assertRaises is assertNotRaises.
---

**Contents**

[TOC]

# assertNotRaises
The opposite of assertRaises is assertNotRaises. This assertion checks that a specific exception is not raised. It is used to verify that the code being tested does not raise an exception when executed.

# Syntax
The syntax for assertNotRaises is as follows:

assertNotRaises(exception, callable, *args, **kwargs)

# Example
For example, the following code checks that the function "foo" does not raise an exception when called with the arguments "a" and "b":

assertNotRaises(Exception, foo, "a", "b")

# Usage
assertNotRaises is typically used in unit tests to check that a piece of code does not raise an exception when executed. It can also be used to check that a certain exception is not raised when a specific set of arguments is passed to a function.
