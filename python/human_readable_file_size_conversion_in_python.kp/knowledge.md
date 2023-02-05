---
title: What is the file size in a readable format for humans?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The function `humanize.naturalsize` can be used to get a human readable version of a file size in Python.
---

**Contents**

[TOC]

# Using os.stat()

The os.stat() function in the Python Standard Library is used to get the file size in bytes. To convert this to a human readable format, the following code can be used:

```python
import os

file_name = "example.txt"
file_stats = os.stat(file_name)
file_size = file_stats.st_size

if file_size < 1024:
    print("File size: %d Bytes" % file_size)
elif 1024 <= file_size < 1048576:
    print("File size: %.2f KB" % (file_size/1024))
elif 1048576 <= file_size < 1073741824:
    print("File size: %.2f MB" % (file_size/1048576))
else:
    print("File size: %.2f GB" % (file_size/1073741824))
```

# Using pathlib

The pathlib module in the Python Standard Library is another way to get the file size. To convert this to a human readable format, the following code can be used:

```python
from pathlib import Path

file_name = Path("example.txt")
file_size = file_name.stat().st_size

if file_size < 1024:
    print("File size: %d Bytes" % file_size)
elif 1024 <= file_size < 1048576:
    print("File size: %.2f KB" % (file_size/1024))
elif 1048576 <= file_size < 1073741824:
    print("File size: %.2f MB" % (file_size/1048576))
else:
    print("File size: %.2f GB" % (file_size/1073741824))
```

# Using glob

The glob module in the Python Standard Library is another way to get the file size. To convert this to a human readable format, the following code can be used:

```python
import glob

file_name = glob.glob("example.txt")[0]
file_size = os.stat(file_name).st_size

if file_size < 1024:
    print("File size: %d Bytes" % file_size)
elif 1024 <= file_size < 1048576:
    print("File size: %.2f KB" % (file_size/1024))
elif 1048576 <= file_size < 1073741824:
    print("File size: %.2f MB" % (file_size/1048576))
else:
    print("File size: %.2f GB" % (file_size/1073741824))
```
