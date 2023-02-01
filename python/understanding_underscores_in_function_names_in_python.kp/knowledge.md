---
title: What is the purpose of having underscores "__" before and after a function name?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The underscores are used to indicate that the function is a `special` or `magic` function, which has special meaning to the interpreter.
---

**Contents**

[TOC]

# Definition

In Python, underscores at the beginning and end of a function name are known as 'dunders' or 'magic' methods. These are special methods that are used by the language to perform specific operations.

# Purpose

The purpose of dunders is to provide a way for Python to distinguish between user-defined functions and built-in functions. This makes it easier for the interpreter to understand and execute code.

# Examples

Examples of dunders include `__init__()`, `__str__()`, and `__len__()`. These are special methods that are used to initialize, print, and get the length of an object, respectively.

# Usage

Dunders are mainly used to override the default behavior of certain operations in Python. For example, the `__add__()` method can be used to define how two objects should behave when added together.
