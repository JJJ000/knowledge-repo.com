---
title: How to set pythonpath to resolve 'unable to import' error in pylint?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Set the PYTHONPATH environment variable to include the directory containing the modules to be imported.
---

**Contents**

[TOC]

1. Introduction

PyLint is a popular Python code analysis tool that checks errors and code quality. It can be used to improve the quality, accuracy, and readability of code. When using PyLint, it is common to encounter an "Unable to import" error if there is a problem with importing a module. In such cases, setting the PYTHONPATH environment variable can be necessary.

2. What is PYTHONPATH?

PYTHONPATH is an environment variable that specifies the list of directories where Python looks for modules when importing them. It is used by Python to locate the modules that are imported in the code. If a module cannot be found, an "Unable to import" error is raised.

3. Setting PYTHONPATH

Setting the PYTHONPATH variable is a simple process. There are two main ways to set this variable:

- Setting PYTHONPATH in the command line:

To set PYTHONPATH in the command line, use the command export PYTHONPATH=/path/to/directory/. Replace "/path/to/directory/" with the path to the directory containing the module that needs to be imported. This command is only valid for the current terminal session.

- Setting PYTHONPATH in the code:

To set PYTHONPATH in the code, use the following command at the beginning of the script:
```python
import sys
sys.path.append("/path/to/directory/")
```
Replace "/path/to/directory/" with the path to the directory containing the module that needs to be imported.

4. Conclusion

The PYTHONPATH environment variable is used by Python to locate modules when importing them. If a module cannot be found, an "Unable to import" error is raised. Setting the PYTHONPATH variable can be done in the command line or in the code using the sys.path.append() command. It is crucial to understand how to set PYTHONPATH to avoid "Unable to import" errors when using PyLint or running Python code.
