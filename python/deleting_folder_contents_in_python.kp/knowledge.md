---
title: What is the process for emptying the contents of a folder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the shutil.rmtree() function to delete the contents of a folder in Python.
---

**Contents**

[TOC]

# Section 1: Import os Library 

In order to delete the contents of a folder in Python, the os library needs to be imported. 

```python
import os
```

# Section 2: Access the Folder

The folder needs to be accessed in order to delete its contents. This can be done by using the os library's `os.chdir()` function. 

```python
os.chdir('/path/to/folder')
```

# Section 3: Delete Contents of Folder

Once the folder has been accessed, its contents can be deleted by using the os library's `os.remove()` function. 

```python
for file in os.listdir():
    os.remove(file)
```

# Section 4: Confirm Deletion

To confirm that the contents of the folder have been deleted, the os library's `os.listdir()` function can be used to list the contents of the folder. 

```python
os.listdir()
```
