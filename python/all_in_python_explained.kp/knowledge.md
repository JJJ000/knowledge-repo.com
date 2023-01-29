---
title: What is the meaning of the keyword '__all__' in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: \_\_all\_\_ is a list of variables or functions that are imported when using the `from module import *` syntax.
---

**Contents**

[TOC]

# Definition
__all__ is a special variable in Python that is used to control which names are imported when from a module is imported using the form from module import *

# Syntax
The syntax for __all__ is to assign a list of strings to the variable, where each string is the name of a variable or submodule to be imported.

# Example
For example, if a module contains the following variables:

x = 1
y = 2
z = 3

__all__ = ['x', 'z']

Then, when from module import * is used, only x and z will be imported.

# Benefits
Using __all__ can help reduce the amount of clutter in the global namespace, as only the names specified in the __all__ list will be imported. It also makes it easier to keep track of which names are being imported from a module.
