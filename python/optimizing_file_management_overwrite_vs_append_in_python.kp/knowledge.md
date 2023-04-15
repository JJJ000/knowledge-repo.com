---
title: Instead of adding at the end, delete and rewrite
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To replace and overwrite instead of appending in Python, you can simply use the assignment operator (=) to assign the new value to the variable.
---

**Contents**

[TOC]

Using "w" mode in Python

The simplest way to replace or overwrite the contents of an existing file in Python is to open it in "w" (write) mode. This mode creates a new empty file if it does not exist, and overwrites the existing file if it does. Here is an example:

```python
with open("myfile.txt", "w") as f:
    f.write("This text will replace the previous content of the file")
```

This code opens the file "myfile.txt" in write mode and writes a new string in it. If the file already existed, its contents are replaced by the new string.

Using "truncate" method

To overwrite a file while keeping its previous contents intact, you can use the "truncate" method. This method sets the file's size to a specified value, deleting any contents beyond that point. Here is an example:

```python
with open("myfile.txt", "r+") as f:
    f.seek(0)  # move the file pointer to the beginning
    f.write("Hello world\n")  # overwrite the first line
    f.truncate()  # delete any lines beyond the first
```

This code opens the file "myfile.txt" in read+write mode, overwrites its first line with a new string, and then deletes any contents beyond that line using the "truncate" method.

Using "os" module

Another way to replace a file's contents is to use the "os" module to delete the existing file and create a new one with the same name. Here is an example:

```python
import os

filename = "myfile.txt"

if os.path.exists(filename):
    os.remove(filename)  # delete the existing file

with open(filename, "w") as f:
    f.write("This text will replace the previous content of the file")
```

This code checks if a file with the name "myfile.txt" exists, deletes it if it does, and then creates a new empty file with the same name using "w" mode. The new file is then populated with the desired contents.
