---
title: What is the method to confirm the version of Python in a program that employs new language features?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the command `python --version` in the command line/terminal to check the Python version.
---

**Contents**

[TOC]

# Introduction 

In order to ensure the compatibility of a program that uses new language features, it is important to check for the version of Python that is being used. This can be done easily within the program itself, allowing the program to take action based on the version of Python that is currently installed on the system. There are several ways to achieve this, which will be outlined in the following sections.

# Using sys.version_info

One way to check the version of Python being used is to use the `sys.version_info` attribute. This is a tuple containing the major, minor and micro version numbers of the current Python interpreter. Here is an example:

```python
import sys

if sys.version_info >= (3, 5):
    # Do something that requires Python 3.5 or later
else:
    # Do something else for earlier versions of Python
```

In this example, if the current Python interpreter is version 3.5 or later, the program will execute the code in the first block. Otherwise, it will execute the code in the second block.

# Using platform.python_version()

Another way to check the version of Python being used is to use the `platform.python_version()` function. This function returns the version of Python as a string. Here is an example:

```python
import platform

if platform.python_version() >= '3.5':
    # Do something that requires Python 3.5 or later
else:
    # Do something else for earlier versions of Python
```

In this example, if the current Python interpreter is version 3.5 or later, the program will execute the code in the first block. Otherwise, it will execute the code in the second block.

# Using the try/except block

A third way to check the version of Python being used is to use a `try`/`except` block to catch any exceptions that might occur due to the use of new language features. Here is an example:

```python
try:
    # Do something that requires Python 3.5 or later
except NameError:
    # Do something else for earlier versions of Python
```

In this example, if the current Python interpreter is version 3.5 or later, the program will execute the code in the `try` block without any errors. However, if the interpreter is an earlier version of Python that does not support the new language features, a `NameError` will be raised and the code in the `except` block will be executed instead.

# Conclusion

In summary, there are several ways to check the version of Python being used within a program that uses new language features. These include using `sys.version_info`, `platform.python_version()` or a `try`/`except` block to catch any exceptions that might occur. By using these methods, you can ensure that your program is compatible with the version of Python currently installed on the system.
