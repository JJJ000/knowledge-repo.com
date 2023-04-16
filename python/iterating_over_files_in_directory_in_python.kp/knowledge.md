---
title: What is the best way to loop through the files in a specific folder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `os.listdir()` function to iterate over the files in a given directory.
---

**Contents**

[TOC]

1. **Import os Module**

The os module provides a number of useful functions that can be used to list files in a directory.

```python
import os
```

2. **List Files in Directory**

To list all files in a directory, use the os.listdir() function. This function takes in the path of the directory and returns a list of filenames.

```python
filenames = os.listdir('/path/to/directory')
```

3. **Iterate Over Files**

Once the list of filenames is obtained, we can iterate over them to perform operations on each file.

```python
for filename in filenames:
    # Perform operations on each file
    # ...
```

4. **Example**

The following example shows how to list all files in a directory and print the filenames.

```python
import os

# List all files in the directory
filenames = os.listdir('/path/to/directory')

# Iterate over files
for filename in filenames:
    # Print filename
    print(filename)
```
