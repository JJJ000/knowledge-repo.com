---
title: How to manipulate environment variables using Python for reading and writing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To read or write environment variables in Python, you can utilize the `os` module, specifically the `os.environ` dictionary.
---

**Contents**

[TOC]

Section 1: Introduction
Python, a high-level programming language, provides support for handling environment variables to access, read, and modify them. Environment variables are globally defined variables that store various system-related information, such as file paths, configuration settings, and user preferences, among other things. You can access environment variables in Python using the built-in `os` module.

Section 2: Reading Environment Variables
You can read environment variables in Python using the `os.environ` dictionary. This dictionary contains key-value pairs of all the environment variables available. You can retrieve the value of a specific environment variable using `os.environ.get('VARIABLE_NAME')`.

```python
import os
print(os.environ.get('HOME'))
```
Output:
```
/Users/username
```
In this example, we are retrieving the value of the `HOME` environment variable, which stores the path to the home directory of the current user.

Section 3: Writing Environment Variables
To write or set environment variables, you can use the `os.environ` dictionary. You can set the value of an environment variable using the `os.environ` dictionary as follows:

```python
import os
os.environ['MY_VAR'] = 'my value'
```
In this example, we are setting the value of the `MY_VAR` environment variable to `'my value'`.

Section 4: Conclusion
In this tutorial, you learned how to use the `os` module in Python to read and write environment variables. Using these functions, you can easily access and modify environment variables from your Python scripts. Environment variables are used extensively in many applications to store various settings and configurations, and having the ability to manipulate them using Python can be extremely useful.
