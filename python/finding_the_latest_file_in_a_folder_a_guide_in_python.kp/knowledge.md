---
title: What's the method to obtain the most recent file present in a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the max() function to get the latest file in a folder based on the file`s creation or modification time.
---

**Contents**

[TOC]

## Getting a list of files in a folder using os module

In order to get the latest file in a folder, we first need to get a list of all the files in that folder. We can do this using the `os` module in Python. Here's how we can use `os.listdir()` function to get a list of all the files in a folder:

```python
import os

folder_path = '/path/to/folder'
files = os.listdir(folder_path)
```

This will give us a list of files in the specified folder.

## Sorting files based on modified time

Once we have a list of files in the folder, we can sort them based on their modification time using the `os.path.getmtime()` function. This function returns the modification time of a file in seconds since the epoch. We can pass this function to the `sorted()` function to sort the list of files based on their modification time. Here's how we can do this:

```python
import os

folder_path = '/path/to/folder'
files = os.listdir(folder_path)

# Sort the files based on modification time
files = sorted(files, key=lambda x: os.path.getmtime(os.path.join(folder_path, x)))
```

This will give us a sorted list of files in the specified folder based on their modification time.

## Getting the latest file

To get the latest file from the sorted list, we can simply retrieve the last element of the list using the index `-1`. Here's how we can do this:

```python
import os

folder_path = '/path/to/folder'
files = os.listdir(folder_path)

# Sort the files based on modification time
files = sorted(files, key=lambda x: os.path.getmtime(os.path.join(folder_path, x)))

# Get the latest file
latest_file = os.path.join(folder_path, files[-1])
```

This will give us the path to the latest file in the specified folder. We can then use this path to open or manipulate the file as required.
