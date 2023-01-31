---
title: What is the equivalent command to 'cd' in the shell to switch the current working directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: os.chdir() can be used to change the current working directory in Python.
---

**Contents**

[TOC]

# os.chdir()
The `os.chdir()` function can be used to change the current working directory in Python. This function takes in a string argument that represents the path of the directory to change to.

# Example
The following code snippet shows an example of how to use the `os.chdir()` function to change the working directory.

```
import os

# Change to the Documents directory
os.chdir('/home/user/Documents')
```

# os.getcwd()
The `os.getcwd()` function can be used to get the current working directory. This function returns a string representing the path of the current working directory.

# Example
The following code snippet shows an example of how to use the `os.getcwd()` function to get the current working directory.

```
import os

# Get the current working directory
current_dir = os.getcwd()

# Print the current working directory
print(current_dir)
```
