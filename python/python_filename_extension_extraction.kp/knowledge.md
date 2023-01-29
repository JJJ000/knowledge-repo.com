---
title: Obtaining the file type from a file name in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The extension of a filename can be extracted from a string using the os.path.splitext() method.
---

**Contents**

[TOC]

# Section 1: Using os.path.splitext
The os.path.splitext function is a useful tool to extract the extension from a filename in Python. This function takes a single argument, which is the filename, and returns a tuple containing the filename and the extension. 

# Section 2: Example
For example, consider the filename “example.txt”. To extract the extension from this filename, we can use the os.path.splitext function as follows:

```python
import os

filename = "example.txt"
name, ext = os.path.splitext(filename)

print(ext)
```

This will print out “.txt”, which is the extension of the filename.

# Section 3: Other Options
In addition to using os.path.splitext, there are other ways to extract the extension from a filename in Python. For example, you can use the string split method to split the filename on the period character, which will return a list of strings containing the filename and extension.

# Section 4: Example
For example, consider the same filename “example.txt”. To extract the extension from this filename, we can use the string split method as follows:

```python
filename = "example.txt"
name, ext = filename.split(".")

print(ext)
```

This will also print out “.txt”, which is the extension of the filename.
