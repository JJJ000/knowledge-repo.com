---
title: What is the way to sort a directory listing by creation date in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `os.listdir()` method along with the `os.path.getctime()` method and sort the result using the `sorted()` method with the `key` argument set to `os.path.getctime`.
---

**Contents**

[TOC]

## Importing required modules

To obtain the directory listing in Python, we need to use the `os` module. To sort the files by date, we will also need the `datetime` module.

```python
import os
from datetime import datetime
```

## Getting the list of files

We can use the `os.listdir()` function to get the list of files in a directory. This function returns the list of files in the given directory in arbitrary order. 

```python
dir_path = '/path/to/directory'
files = os.listdir(dir_path)
```

## Sorting files by creation date

To sort the files by creation date, we need to get the file's creation time using `os.path.getctime()` function. We can create a list of tuples with the filename and its creation time, sort it by the creation time, and then extract only the filenames in the desired order.

```python
file_times = [(f, os.path.getctime(os.path.join(dir_path, f))) for f in files]
sorted_files = sorted(file_times, key=lambda x: x[1])
sorted_filenames = [f[0] for f in sorted_files]
```

The `sorted()` function takes an optional `key` parameter - this is a function that would be applied to each element of the list and the resulting value would be used for sorting. In our case, we use a lambda function that returns the second element of the tuple, which is the file's creation time.

## Full code

Putting it all together, the full code to get a list of files sorted by creation date in Python looks like this:

```python
import os
from datetime import datetime

dir_path = '/path/to/directory'
files = os.listdir(dir_path)

file_times = [(f, os.path.getctime(os.path.join(dir_path, f))) for f in files]
sorted_files = sorted(file_times, key=lambda x: x[1])
sorted_filenames = [f[0] for f in sorted_files]
```

Now `sorted_filenames` contains the list of files in `dir_path` sorted by their creation time.
