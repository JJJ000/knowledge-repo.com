---
title: What is the process to obtain the complete path of a pathlib.path object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `.resolve()` method on the pathlib.Path object to get its absolute path.
---

**Contents**

[TOC]

# Section 1: Introduction
In Python, the `pathlib` module provides an object-oriented approach to dealing with files and folders. One common task when working with files and folders is to get the absolute path of a file or folder. In this tutorial, we will discuss how to get the absolute path of a `pathlib.Path` object in Python.

# Section 2: Getting the absolute path using the absolute() method
The `pathlib.Path` class provides a method called `absolute()` that returns the absolute path of the file or folder. Here is an example:

```python
from pathlib import Path

# create a Path object
file_path = Path("file.txt")

# get the absolute path
abs_path = file_path.absolute()

# print the absolute path
print(abs_path)
```

Output:
```
C:\Users\John\file.txt
```

In this example, we first create a `Path` object using the `Path()` constructor. Then, we call the `absolute()` method on the `file_path` object to get the absolute path. Finally, we print the absolute path using the `print()` function.

# Section 3: Getting the absolute path using the resolve() method
Another method provided by the `Path` class to get the absolute path is `resolve()`. This method resolves any symlinks or relative paths to return the absolute path. Here is an example:

```python
from pathlib import Path

# create a Path object
file_path = Path("file.txt")

# get the absolute path using resolve()
abs_path = file_path.resolve()

# print the absolute path
print(abs_path)
```

Output:
```
C:\Users\John\file.txt
```

In this example, we first create a `Path` object using the `Path()` constructor. Then, we call the `resolve()` method on the `file_path` object to get the absolute path. Finally, we print the absolute path using the `print()` function.

# Section 4: Conclusion
In this tutorial, we discussed how to get the absolute path of a `pathlib.Path` object in Python. We learned that the `Path` class provides two methods, `absolute()` and `resolve()`, to get the absolute path. The `absolute()` method simply returns the absolute path, while the `resolve()` method resolves any symlinks or relative paths before returning the absolute path.
