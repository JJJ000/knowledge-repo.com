---
title: Rename multiple files within a folder using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the os.rename() function to rename multiple files in a directory in Python.
---

**Contents**

[TOC]

# Method 1: Using os.rename()

The os.rename() method can be used to rename multiple files in a directory. This method takes two arguments, the old name and the new name. To rename multiple files, loop through all the files in the directory and call os.rename() on each file.

```python
import os 

# Path of the directory 
path = 'C:/Users/User/Documents/'

# List all the files in the directory 
files = os.listdir(path) 

# Iterate over each file 
for file in files: 
	# Separate the file name and its extension 
	filename, file_extension = os.path.splitext(file) 

	# Rename the file 
	os.rename(os.path.join(path, file), os.path.join(path, filename + '_new' + file_extension)) 
```

# Method 2: Using shutil.move()

The shutil.move() method can be used to rename multiple files in a directory. This method takes two arguments, the source path and the destination path. To rename multiple files, loop through all the files in the directory and call shutil.move() on each file.

```python
import shutil 

# Path of the directory 
path = 'C:/Users/User/Documents/'

# List all the files in the directory 
files = os.listdir(path) 

# Iterate over each file 
for file in files: 
	# Separate the file name and its extension 
	filename, file_extension = os.path.splitext(file) 

	# Rename the file 
	shutil.move(os.path.join(path, file), os.path.join(path, filename + '_new' + file_extension)) 
```
