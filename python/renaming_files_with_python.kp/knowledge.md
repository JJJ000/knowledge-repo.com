---
title: What is the process for renaming a file using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the os.rename() function to rename a file using Python.
---

**Contents**

[TOC]

# Section 1 - Importing the os module 

In order to rename a file using Python, we must first import the os module. This module provides a portable way of using operating system dependent functionality. 

```python
import os
```

# Section 2 - Path to the File 

Next, we must specify the path to the file we want to rename. This can be done using the os.path.join() function. This function takes two arguments, the first being the directory path and the second being the file name. 

```python
file_path = os.path.join("directory_path", "old_file_name")
```

# Section 3 - Renaming the File 

Now that the path to the file is specified, we can use the os.rename() function to rename the file. This function takes two arguments, the first being the path to the old file and the second being the path to the new file. 

```python
os.rename(file_path, "new_file_name")
```

# Section 4 - Verifying the Rename 

Finally, we can verify that the file was successfully renamed by using the os.path.exists() function. This function takes a single argument, which is the path to the file. If the file exists, the function will return True, otherwise it will return False. 

```python
os.path.exists("new_file_name")
```
