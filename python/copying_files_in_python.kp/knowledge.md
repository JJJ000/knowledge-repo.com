---
title: What is the process for copying files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: To copy files in Python, use the `shutil.copy()` function.
---

**Contents**

[TOC]

### Using the shutil Module
The shutil module provides a number of high-level operations on files and collections of files. It can be used to copy files between directories.

### Syntax
The syntax for copying files with the shutil module is as follows:

```python
shutil.copy(source, destination)
```

### Example
The following example copies a file from the current directory to the specified destination directory:

```python
import shutil

src = 'source_file.txt'
dst = 'destination_directory/'

shutil.copy(src, dst)
```

### Additional Parameters
The shutil module also provides additional parameters for copying files, such as the ability to preserve file metadata and permissions. For more information, please refer to the [Python documentation](https://docs.python.org/3.7/library/shutil.html).
