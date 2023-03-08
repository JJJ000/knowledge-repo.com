---
title: In python, what is the method to retrieve the folder path from a file path?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the built-in os module in Python to extract the folder path from a file path.
---

**Contents**

[TOC]

## Splitting the file path string
In order to extract the folder path from a file path in Python, we can use the `os.path` module. The first step is to split the file path string using the `os.path.split()` function. This function returns a tuple containing the directory path and the file name. We then need to further split the directory path to get the folder path.

```python
import os

file_path = "/path/to/file.txt"
dir_path, file_name = os.path.split(file_path)
print(dir_path)  # output: /path/to
```

## Getting the folder path
We can use the `os.path.dirname()` function to get the folder path from the directory path. This function takes the directory path as argument and returns the parent directory path.

```python
import os

file_path = "/path/to/file.txt"
dir_path, file_name = os.path.split(file_path)
folder_path = os.path.dirname(dir_path)
print(folder_path)  # output: /path
```

## Handling different file path separators
If the file path contains different path separators (e.g. backslashes instead of forward slashes), we need to ensure that our code works on different operating systems. We can use the `os.path.normpath()` function to normalize the path separators.

```python
import os

file_path = "C:\\path\\to\\file.txt"
dir_path, file_name = os.path.split(file_path)
folder_path = os.path.dirname(os.path.normpath(dir_path))
print(folder_path)  # output: C:\path
```

## Conclusion
In summary, we can extract the folder path from a file path in Python by splitting the file path string, getting the directory path, and using the `os.path.dirname()` function to get the parent directory path. Additionally, we should use the `os.path.normpath()` function to ensure that our code works on different operating systems.
