---
title: What is the operating system for the Python program?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: The sys module can be used to identify the operating system Python is running on.
---

**Contents**

[TOC]

# Section 1: Using the sys Module
The sys module in Python provides access to system-specific parameters and functions. This module can be used to identify which OS Python is running on.

# Section 2: Accessing sys.platform
The sys.platform attribute contains the name of the operating system platform that the Python interpreter is running on. This attribute can be used to identify the OS Python is running on.

# Section 3: Example
The following example demonstrates how to use the sys.platform attribute to identify the OS Python is running on:

```python
import sys

if sys.platform == 'win32':
    print('You are running Windows.')
elif sys.platform == 'darwin':
    print('You are running macOS.')
elif sys.platform == 'linux':
    print('You are running Linux.')
```

# Section 4: Output
The output of the above code will be one of the following, depending on the OS Python is running on:

- You are running Windows.
- You are running macOS.
- You are running Linux.
