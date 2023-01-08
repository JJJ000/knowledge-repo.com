---
title: How do I check file existence without exceptions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: You can use the `os.path.exists()` function to check if a file exists without raising exceptions.
---

**Contents**

[TOC]

### Using the os.path Module
The `os.path` module provides functions to check if a file or directory exists.

### os.path.exists()
The `os.path.exists()` method can be used to check if a file or directory exists. It returns `True` if the file or directory exists, and `False` if not.

```python
import os.path

if os.path.exists("myfile.txt"):
#    print("File exists")
else:
#    print("File does not exist")
```

### os.path.isfile()
The `os.path.isfile()` method can be used to check if a file exists. It returns `True` if the file exists, and `False` if not.

```python
import os.path

if os.path.isfile("myfile.txt"):
#    print("File exists")
else:
#    print("File does not exist")
```

### os.path.isdir()
The `os.path.isdir()` method can be used to check if a directory exists. It returns `True` if the directory exists, and `False` if not.

```python
import os.path

if os.path.isdir("mydir"):
#    print("Directory exists")
else:
#    print("Directory does not exist")
```
