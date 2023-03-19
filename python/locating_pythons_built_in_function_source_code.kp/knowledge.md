---
title: How can one locate the source code of python's pre-installed functions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The built-in Python functions are written in C and their source code can be found in the CPython repository on GitHub.
---

**Contents**

[TOC]

Section 1: Overview
Python comes with many built-in functions that can be directly used in any Python program. Some of these functions include print(), len(), int(), str(), and more. While the functionality of these functions is well-documented, sometimes it's necessary to look at the underlying source code to understand how they work or to modify them to better suit your application's needs.

Section 2: Using the inspect module
Python's inspect module provides a way to programmatically look at the source code of a built-in function. To use it, you first need to import the module:

```
import inspect
```

From there, you can use the getsource() function to retrieve the source code for a given function. For example, to get the source code for the print() function, you would use the following code:

```
import inspect

source_code = inspect.getsource(print)
```

The source_code variable now contains the full source code for the print() function.

Section 3: Using the dis module
Another way to look at the source code of built-in Python functions is to use the dis module. This module disassembles Python bytecode and provides a human-readable representation of the resulting instructions. To use it, you can pass the function you're interested in to the dis.dis() function. For example, to disassemble the int() function, you would use the following code:

```
import dis

dis.dis(int)
```

This would output the disassembled bytecode for the int() function.

Section 4: Can't view the source code for all built-in functions
It's worth noting that not all built-in functions have source code that you can view. Some functions are implemented as C functions and do not have corresponding Python code. In these cases, you will not be able to use the above methods to view the source code.
