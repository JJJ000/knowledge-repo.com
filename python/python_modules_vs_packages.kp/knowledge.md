---
title: What is the distinction between a Python module and a Python package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: A Python module is a single file containing Python code, while a Python package is a directory of Python modules containing an additional \_\_init\_\_.py file.
---

**Contents**

[TOC]

# Module
A Python module is a single Python file that can contain functions, classes, and variables. It is used to organize related code into one file.

# Package
A Python package is a collection of modules in directories that give a package hierarchy. It allows for a logical way to structure Python’s module namespace by using “dotted module names”. A package can contain sub-packages and modules while the sub-packages can also contain further sub-packages and modules. Packages can be imported the same way modules are imported.
