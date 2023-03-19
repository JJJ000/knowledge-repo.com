---
title: What is the way to obtain the path of the currently run file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the `os` module in Python and the `\_\_file\_\_` attribute to get the path of the currently executed file.
---

**Contents**

[TOC]

## Using __file__ attribute

The `__file__` attribute in Python returns the path of the current executed file. Here's how you can use it:

```python
import os

current_file_path = os.path.abspath(__file__)
print(current_file_path)
```

The `os.path.abspath()` function returns the absolute path of the file.

## Using inspect module

Another way to get the path of the current executed file is to use the `inspect` module.

```python
import inspect

current_file_path = inspect.getfile(inspect.currentframe())
print(current_file_path)
```

The `inspect.getfile()` function returns the file name from which the specified function was loaded. In this case, we are using `inspect.currentframe()` to get the current frame object.

## Using sys.argv

`sys.argv` is a list in Python that contains the command-line arguments passed to the script. The first element of `sys.argv` is always the name of the script itself.

```python
import sys

current_file_path = sys.argv[0]
print(current_file_path)
```

In this case, we are using the first element of `sys.argv` to get the path of the current executed file.

## Using pathlib module

The `pathlib` module in Python provides an intuitive way to work with file paths.

```python
from pathlib import Path

current_file_path = Path(__file__).resolve()
print(current_file_path)
```

Here, we are creating a `Path` object with `__file__` attribute, and then resolving the absolute path of the file with `resolve()` method.
