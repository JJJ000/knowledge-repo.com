---
title: What is the procedure to access all files in a particular folder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use a loop to iterate through each file in the folder and then open each file with the appropriate method.
---

**Contents**

[TOC]

# Section 1: Importing required libraries
To open every file in a folder in Python, we need to first import the required libraries for working with files and folders. In Python, we have the `os` and `glob` modules for this purpose.


```python
import os
import glob
```

# Section 2: Getting list of files in a folder
We can use the `glob` module to get a list of all files in a folder. The `glob.glob()` method takes a path pattern as input and returns a list of all files that match the pattern. If we want to get all files in a folder, we can use the `*` wildcard character as the pattern.


```python
folder_path = "path/to/folder"
file_list = glob.glob(folder_path + "/*")
```

In the above code, we have specified the `folder_path` variable to the path of the folder for which we want the list of files. Then, we have used the `glob.glob()` method to get a list of all files in the folder.

# Section 3: Opening each file
Once we have the list of files, we can loop through each file and open it one by one. We can use the built-in `open()` function in Python to open each file.


```python
for file_path in file_list:
    with open(file_path, "r") as file:
        # Do something with the file
```

In the above code, we have used a `for` loop to loop through each file in the `file_list`. For each file, we have used the `open()` function to open it in read mode (`"r"`). We have also used a `with` statement to ensure that the file is properly closed after we are done using it. Within the loop, we can perform any operations that we want to perform on each file.

# Section 4: Complete code
```python
import os
import glob

folder_path = "path/to/folder"
file_list = glob.glob(folder_path + "/*")

for file_path in file_list:
    with open(file_path, "r") as file:
        # Do something with the file
```

The complete code above shows how we can open every file in a folder in Python. We first import the required libraries, then get a list of all files in the folder using `glob.glob()`, and then loop through each file and open it using `open()`. Within the loop, we can perform any operations that we want to perform on each file.
