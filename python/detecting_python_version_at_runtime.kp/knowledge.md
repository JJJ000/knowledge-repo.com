---
title: What is the Python version being used while the program is running?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the sys.version attribute to detect the Python version at runtime.
---

**Contents**

[TOC]

1. # Using the `sys` Module
The `sys` module provides access to information about the Python interpreter such as its version. To get the version of Python, use the `sys.version` attribute.

```python
import sys

print(sys.version)
```

2. # Using the `platform` Module
The `platform` module provides access to system and hardware information such as the Python version. To get the version of Python, use the `platform.python_version()` method.

```python
import platform

print(platform.python_version())
```

3. # Using the `subprocess` Module
The `subprocess` module provides access to the command line. To get the version of Python, use the `subprocess.check_output()` method to execute the `python --version` command.

```python
import subprocess

print(subprocess.check_output(["python", "--version"]))
```

4. # Using the `py_version_info` Function
The `py_version_info` function provides access to the Python version information as a tuple. To get the version of Python, use the `py_version_info()` function.

```python
import sys

print(sys.py_version_info())
```
