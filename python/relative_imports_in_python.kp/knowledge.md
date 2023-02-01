---
title: What is the process for performing relative imports in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Relative imports in Python can be done by using the `from . import` syntax.
---

**Contents**

[TOC]

# Section 1: Overview

Relative imports in Python allow you to import modules from a relative path, rather than an absolute path. This is useful for when you want to import modules from the same directory or a subdirectory.

# Section 2: Syntax

The syntax for relative imports in Python is as follows:

`from . import <module>`

This syntax will import the specified module from the same directory as the current file. To import from a subdirectory, the syntax is:

`from ..<subdirectory> import <module>`

# Section 3: Example

For example, if you have a file `foo.py` in the same directory as `bar.py`, you can import `foo` from `bar` using the following syntax:

`from . import foo`

# Section 4: Notes

It is important to note that relative imports are only supported in Python 2.5 and above. In earlier versions of Python, you must use absolute imports.
