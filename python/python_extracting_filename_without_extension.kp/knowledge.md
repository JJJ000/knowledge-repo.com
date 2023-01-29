---
title: What is the syntax for extracting the filename without the extension from a path in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the os.path.splitext() function.
---

**Contents**

[TOC]

**Section 1: Using os.path Module**

The `os.path` module provides several useful functions to manipulate file path names. The `os.path.splitext()` function can be used to split the pathname into a pair (root, ext) containing the filename without extension and the extension respectively.

```python
import os
file_path = 'C:/Users/Desktop/example.txt'
root, ext = os.path.splitext(file_path)
print(root) 
# Output: C:/Users/Desktop/example
```

**Section 2: Using Pathlib Module**

The `pathlib` module is a powerful module that provides an object-oriented approach to working with files and directories. The `Path.stem` method can be used to get the filename without the extension.

```python
from pathlib import Path
file_path = Path('C:/Users/Desktop/example.txt')
filename = file_path.stem
print(filename) 
# Output: example
```

**Section 3: Using Regular Expressions**

Regular expressions can also be used to get the filename without the extension. The `re.search()` function can be used to search for a pattern in a string and the `group()` function can be used to get the matched string.

```python
import re
file_path = 'C:/Users/Desktop/example.txt'
filename = re.search('(\w+)\.\w+$', file_path).group(1)
print(filename) 
# Output: example
```

**Section 4: Using String Slicing**

String slicing can also be used to get the filename without the extension. The `rfind()` method can be used to find the index of the last occurrence of a substring in the string and then the string can be sliced up to that index to get the filename without the extension.

```python
file_path = 'C:/Users/Desktop/example.txt'
filename = file_path[:file_path.rfind('.')]
print(filename) 
# Output: C:/Users/Desktop/example
```
