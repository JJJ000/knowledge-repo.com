---
title: How does os.path.basename() differ from os.path.dirname()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: os.path.basename() returns the base filename in a given path while os.path.dirname() returns the directory portion of the path.
---

**Contents**

[TOC]

# What are os.path.basename() and os.path.dirname() functions?
os.path.basename() and os.path.dirname() are two functions available in the OS module of Python. These functions are used to extract important components of file paths such as file names or directories. 

## os.path.basename() function
The os.path.basename() function returns the final component of a file path, i.e., the file name. This function strips away the directory information from a path and only outputs the file name itself. This function does not check whether the file exists or not.

## os.path.dirname() function
The os.path.dirname() function returns the directory component of a file path, i.e., the directory name. This function strips away the filename from a path and only outputs the directory name itself. This function does not check whether the path exists or not.

# Example Usage
For example, let's assume the path is /Users/johndoe/Desktop/python/file.txt

```python
import os

print(os.path.basename('/Users/johndoe/Desktop/python/file.txt'))
# Output: file.txt

print(os.path.dirname('/Users/johndoe/Desktop/python/file.txt'))
# Output: /Users/johndoe/Desktop/python
```

In the first example, the basename function returned 'file.txt' because it only extracted the file name attribute of the path. In contrast, the second example provides only the directory name component because the dirname function parsed away the file name. 

It is essential to remember that no checks are made on the existence of the file or directory in the file system, and both functions only analyze the input string using string manipulations.
