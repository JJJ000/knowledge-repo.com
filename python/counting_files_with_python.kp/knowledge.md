---
title: What is the Python code to count the number of files in a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the os.listdir() function to count the number of files in a directory.
---

**Contents**

[TOC]

# 1. Import the os module

The `os` module contains functions related to the operating system. We need to import it in order to access the functions for counting files in a directory.

```python
import os
```

# 2. Get the list of files

We can use the `listdir` function from the `os` module to get a list of all the files in a directory. This function takes the path of the directory as its argument.

```python
files = os.listdir('path/to/directory')
```

# 3. Count the files

We can use the `len` function to count the number of items in the list of files.

```python
num_files = len(files)
```

# 4. Print the result

Finally, we can print the result to the console.

```python
print('Number of files:', num_files)
```
