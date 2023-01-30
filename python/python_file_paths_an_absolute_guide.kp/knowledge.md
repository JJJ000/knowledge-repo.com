---
title: What is the procedure for obtaining an absolute file path in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the os.path.abspath() function to get an absolute file path in Python.
---

**Contents**

[TOC]

#1 Using os.path

The os.path module provides functions for working with file and directory paths. The `os.path.abspath()` method can be used to get the absolute file path of a given file.

#2 Syntax

The syntax for using the `os.path.abspath()` method is as follows:

```
os.path.abspath(path)
```

#3 Parameters

The `os.path.abspath()` method takes a single argument, which is the file path that you want to convert to an absolute path.

#4 Example

The following example shows how to use the `os.path.abspath()` method to get the absolute file path of a file:

```
import os

file_path = 'C:/Users/John/Documents/test.txt'
abs_path = os.path.abspath(file_path)

print(abs_path)
```

The output of the above code will be:

`C:\Users\John\Documents\test.txt`
