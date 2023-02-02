---
title: How to write the output of a Python program to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Redirecting stdout to a file in Python can be done by using the `sys.stdout = open(`file\_name`, `w`)` command.
---

**Contents**

[TOC]

# Section 1 - Using the sys Module

The sys module provides access to system-specific parameters and functions. To redirect stdout to a file, use the sys.stdout.write() function.

```python
import sys

# Open a file for writing
f = open('output.txt', 'w')

# Redirect stdout to this file
sys.stdout = f

# Print something to the file
print('This will be printed to the file')

# Close the file
f.close()
```

# Section 2 - Using the contextlib Module

The contextlib module provides a context manager for redirecting stdout to a file.

```python
import contextlib

with open('output.txt', 'w') as f:
    with contextlib.redirect_stdout(f):
        print('This will be printed to the file')
```

# Section 3 - Using the os Module

The os module provides access to operating system functions and can be used to redirect stdout to a file.

```python
import os

# Open a file for writing
f = open('output.txt', 'w')

# Redirect stdout to this file
os.dup2(f.fileno(), sys.stdout.fileno())

# Print something to the file
print('This will be printed to the file')

# Close the file
f.close()
```

# Section 4 - Using the subprocess Module

The subprocess module provides access to functions for running system commands. To redirect stdout to a file, use the subprocess.Popen() function.

```python
import subprocess

# Open a file for writing
f = open('output.txt', 'w')

# Redirect stdout to this file
p = subprocess.Popen(['echo', 'This will be printed to the file'], stdout=f)

# Wait for the process to finish
p.wait()

# Close the file
f.close()
```
