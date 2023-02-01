---
title: What is the location of the script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the os.path.dirname() function to get the directory of a script in Python.
---

**Contents**

[TOC]

# Section 1: Using os.path.dirname()
The `os.path.dirname()` function can be used to find the directory of a script in Python. This function takes in a file path as a parameter and returns the directory of the file path.

# Section 2: Using __file__
The `__file__` attribute can be used to find the directory of a script in Python. This attribute contains the path to the script and can be used with `os.path.dirname()` to get the directory of the script.

# Section 3: Using sys.argv[0]
The `sys.argv[0]` attribute can be used to find the directory of a script in Python. This attribute contains the path to the script and can be used with `os.path.dirname()` to get the directory of the script.

# Section 4: Using os.path.abspath()
The `os.path.abspath()` function can be used to find the absolute path of a script in Python. This function takes in a file path as a parameter and returns the absolute path of the file path. It can be used with `os.path.dirname()` to get the directory of the script.
