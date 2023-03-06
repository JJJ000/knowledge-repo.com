---
title: Change the working directory of Python script to the directory in which the script is located
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the code `os.chdir(os.path.dirname(\_\_file\_\_))` to change the working directory to the directory where the current Python script is located.
---

**Contents**

[TOC]

### Introduction

In Python, if we want to change the script's working directory to the script's own directory, we can use some built-in modules and functions to accomplish this task easily. In this article, we will discuss these methods briefly.

### Method 1: os Module

The `os` module in Python provides us with a lot of functions to interact with the operating system's file system. We can use the `os.getcwd()` function to get the current working directory and `os.chdir()` function to change the working directory. Here's an example:

```
import os

# Get the current working directory
current_dir = os.getcwd()

# Change the working directory to the script's directory
script_dir = os.path.dirname(os.path.abspath(__file__))
os.chdir(script_dir)
```

### Method 2: pathlib Module

The `pathlib` module in Python provides an object-oriented way of working with the file system. We can use the `Path.cwd()` method to get the current working directory and `Path(__file__).parent.resolve()` to get the script's directory. Here's an example:

```
from pathlib import Path

# Get the current working directory
current_dir = Path.cwd()

# Change the working directory to the script's directory
script_dir = Path(__file__).parent.resolve()
os.chdir(str(script_dir))
```

### Method 3: sys Module

The `sys` module in Python provides access to some variables that are maintained by the interpreter and to functions that interact strongly with the interpreter. We can use the `sys.path[0]` to get the path of the script's directory and then change the working directory using the `os.chdir()` function. Here's an example:

```
import os
import sys

# Get the script's directory
script_dir = os.path.dirname(os.path.abspath(sys.path[0]))

# Change the working directory to the script's directory
os.chdir(script_dir)
```

### Conclusion

In this article, we have discussed three different methods to change the script's working directory to the script's own directory. Depending on the situation, we can use any of these methods to achieve the desired result.
