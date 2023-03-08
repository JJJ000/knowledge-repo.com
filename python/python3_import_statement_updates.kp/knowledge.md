---
title: Modifications to the import statement in Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: In Python3, the import statement is the same as in Python2, but the behavior of the import statement has some differences.
---

**Contents**

[TOC]

Section 1: Introduction 
Python 3 introduces some changes in the import statement which has been done to make it more efficient and easier for developers.

Section 2: Absolute and Relative Imports 
In Python 2.x, there was no distinction between absolute and relative imports. However, in Python 3, you can use the 'from .Module import' syntax to import a module from the same package directory. In contrast, you can use the 'from Package.Module import' syntax to import a module from a package directory.

Section 3: Parentheses for Import Statement 
In Python 3, parentheses are optional in the import statement. You can write import statements with or without parentheses, and both are valid. For example-
import math is equivalent to import (math).

Section 4: Namespace Packages 
Namespace packages are a new feature introduced in Python 3. They are used to merge multiple directories containing Python modules under a single package namespace. For example, a directory named 'utils_package' could contain modules such as 'string', 'file', and 'array'. These modules could be accessed as utils_package.string, utils_package.file, and utils_package.array.

Overall, these changes in import statements in Python3 make it more efficient and easier to use for developers.
