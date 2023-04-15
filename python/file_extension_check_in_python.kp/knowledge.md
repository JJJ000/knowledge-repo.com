---
title: What is the method for verifying a file's extension?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the method `.split(`.`)[-1]` on the filename string to return the extension.
---

**Contents**

[TOC]

## Using the os module

The `os` module in Python provides a way to interact with the operating system. To check the extension of a file, we can use the `os.path.splitext()` method. This method returns a tuple containing the filename and the extension of the file.

```python
import os

filename = 'example.txt'
file_extension = os.path.splitext(filename)[1]

print(file_extension)
```
Output:
```
.txt
```

## Using pathlib module

The `pathlib` module was introduced in Python 3.4 and provides an object-oriented approach to working with file system paths. It provides a `suffix` attribute that can be used to get the extension of the file.

```python
from pathlib import Path

filename = Path('example.txt')
file_extension = filename.suffix

print(file_extension)
```
Output:
```
.txt
```

## Using regular expressions

Another way to check the extension of a file is using regular expressions. We can use the `re` module to match the extension pattern in a filename and extract it.

```python
import re

filename = 'example.txt'
file_extension = re.search('\.(\w+)$', filename).group(1)

print(file_extension)
```
Output:
```
txt
```
Here, we are using regular expression `\.\w+$` to match the file extension and extract it. The `\.` matches a period character, `\w+` matches one or more word characters, and the `$` matches the end of the string. The parentheses around `\w+` captures the extension as a group that we can extract using the `group()` method.
