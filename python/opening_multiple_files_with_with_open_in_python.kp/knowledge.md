---
title: What is the syntax for opening multiple files using "with open" in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can open multiple files using `with open` in Python by using multiple `with open` statements.
---

**Contents**

[TOC]

### Section 1: Using for loop

The easiest way to open multiple files using `with open` in Python is to use a `for` loop. The loop can iterate through a list of file names and open each file. 

### Section 2: Code example

Below is an example of how to use a `for` loop to open multiple files using `with open`.

```
filenames = ['file1.txt', 'file2.txt', 'file3.txt']

for filename in filenames:
    with open(filename) as f:
        # do something with the file
```

### Section 3: Using contextlib

Another way to open multiple files using `with open` in Python is to use the `contextlib` module. This module provides a context manager for multiple files, allowing you to open multiple files with a single `with` statement.

### Section 4: Code example

Below is an example of how to use `contextlib` to open multiple files using `with open`.

```
from contextlib import ExitStack

filenames = ['file1.txt', 'file2.txt', 'file3.txt']

with ExitStack() as stack:
    files = [stack.enter_context(open(filename)) for filename in filenames]
    # do something with the files
```
