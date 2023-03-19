---
title: Can you find a different way to describe the function called 'seek'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The seek() function in Python is used to change the current position or offset of the file pointer within a file.
---

**Contents**

[TOC]

## Overview

In Python, the `seek()` function is used to change the position of the file handle in a file, allowing the user to read or write data at a specific location in the file. 

The `seek()` function requires one argument, the offset, which represents the number of bytes to move the file handle. 

It returns the new position of the file handle after it has been moved.

## Syntax

```python
file_obj.seek(offset[, whence])
```

The `offset` parameter specifies the number of bytes to move the file pointer.

The `whence` parameter is optional and defaults to `0` (the beginning of the file). It also accepts two other values:

* `1`: current position in the file.
* `2`: end of the file.


## Examples

### Example 1: Moving the File Pointer to the Beginning of the File

```python
with open('file.txt', 'r') as file:
    # read the first line
    line1 = file.readline()

    # move the file pointer to the beginning of the file
    file.seek(0)

    # read the entire file
    content = file.read()

print(line1)  # prints the first line of the file
print(content)  # prints the entire file
```

### Example 2: Moving the File Pointer to a Specific Location

```python
with open('file.txt', 'r') as file:
    # move the file pointer to the 10th byte in the file
    file.seek(10)

    # read the next 10 bytes
    content = file.read(10)

print(content)  # prints the 10 bytes after the 10th byte
```
