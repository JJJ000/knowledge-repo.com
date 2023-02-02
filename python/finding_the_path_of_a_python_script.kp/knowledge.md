---
title: What is the location of the Python script I am currently executing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The path of the Python script can be obtained using the \_\_file\_\_ variable.
---

**Contents**

[TOC]

# Section 1: Using __file__

The `__file__` variable stores the path of the current Python script. To get the path of the script, simply print the value of `__file__`:

```python
print(__file__)
```

# Section 2: Using sys.argv

The `sys.argv` list stores the command line arguments passed to the Python script. The first element of the list (`sys.argv[0]`) stores the path of the script:

```python
import sys
print(sys.argv[0])
```

# Section 3: Using os.path.realpath

The `os.path.realpath` function returns the canonical path of the given path. To get the path of the current script, simply pass `__file__` to `os.path.realpath`:

```python
import os
print(os.path.realpath(__file__))
```

# Section 4: Using os.path.abspath

The `os.path.abspath` function returns the absolute path of the given path. To get the path of the current script, simply pass `__file__` to `os.path.abspath`:

```python
import os
print(os.path.abspath(__file__))
```
