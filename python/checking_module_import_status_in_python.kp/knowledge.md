---
title: What is the way to verify if a module has been imported?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can check if a module has been imported in Python by using the `in` keyword and checking if the module name is in the list of imported modules (sys.modules).
---

**Contents**

[TOC]

# Introduction 
In Python, you can check if a module has been imported or not. In this tutorial, we will discuss a few ways to check if a module has been imported in Python.

# Using the 'sys' module
The 'sys' module in Python provides access to some variables used or maintained by the interpreter and to functions that interact with the interpreter.
We can check if a module has been imported or not using the following code:

```
import sys
 
if 'module_name' in sys.modules:
    print('Module has been imported')
else:
    print('Module has not been imported')
```

# Using 'importlib'
The 'importlib' module provides more sophisticated tools for importing modules than the built-in import statement. We can use the 'find_loader' method to check if the module has been imported or not.

```
import importlib
 
if importlib.find_loader('module_name'):
    print('Module has been imported')
else:
    print('Module has not been imported')
```

# Using 'globals'
Python has a built-in function called 'globals' that returns a dictionary representing the current global symbol table. We can use this function to check if a module has been imported or not.

```
if 'module_name' in globals():
    print('Module has been imported')
else:
    print('Module has not been imported')
```

# Conclusion
In this tutorial, we discussed three ways to check if a module has been imported in Python. By using 'sys', 'importlib', and 'globals' methods, you can easily check if a module has been imported or not.
