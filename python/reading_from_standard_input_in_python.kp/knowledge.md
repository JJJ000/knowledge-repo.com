---
title: What is the process for reading from standard input?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To read from stdin in Python, use the built-in function input().
---

**Contents**

[TOC]

# Reading from Standard Input

## Using sys.stdin
Python provides a built-in module called sys that contains many system-level functions and variables. The sys.stdin variable contains the standard input stream, which can be read using the read() method.

```python
import sys

# Read a line from stdin
line = sys.stdin.readline()

# Read all lines from stdin
lines = sys.stdin.readlines()
```

## Using input()
The input() function can be used to read a line from standard input.

```python
# Read a line from stdin
line = input()
```

## Using fileinput
The fileinput module provides an easy way to read lines from standard input or from a list of files.

```python
import fileinput

# Read a line from stdin
line = fileinput.input().readline()

# Read all lines from stdin
lines = fileinput.input().readlines()
```
