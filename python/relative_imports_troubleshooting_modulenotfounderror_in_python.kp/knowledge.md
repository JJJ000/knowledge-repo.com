---
title: Error no module named x found when trying to use a relative import
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Relative imports allow Python programs to reference modules in parent or sibling directories, but the module must be in the same directory or a parent/sibling directory in order for the import to succeed.
---

**Contents**

[TOC]

# What are Relative Imports?
Relative imports are a way to import modules or packages that are located in the same directory as the current file. Relative imports are used when the modules or packages to be imported are not in the same directory as the file that is importing them.

# What is a ModuleNotFoundError?
A ModuleNotFoundError is an error that is raised when a Python module or package cannot be located in the directory specified by the import statement. This error is raised when the module or package that is being imported is not in the same directory as the file that is importing it.

# How to Fix ModuleNotFoundError in Python?
1. Check the spelling of the module or package name: Make sure that the module or package name is spelled correctly.

2. Check the directory path: Make sure that the directory path specified in the import statement is correct.

3. Use absolute imports: If the module or package is not in the same directory as the file that is importing it, use absolute imports instead of relative imports. Absolute imports specify the full path of the module or package to be imported.
