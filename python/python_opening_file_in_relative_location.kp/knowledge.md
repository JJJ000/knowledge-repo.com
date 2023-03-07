---
title: Python code that accesses a file situated in a location that is relative
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To open a file in a relative location in Python, you can use the `./` notation to specify a relative path from the current working directory.
---

**Contents**

[TOC]

Section 1: Understanding absolute and relative file paths

Before we dive into how to open a file in a relative location in Python, it's important to understand what absolute and relative file paths are.

An absolute file path is a file path that starts from the root directory of the file system. For example, in a Unix-based system, an absolute file path might look like this: `/home/user/Documents/file.txt`. This file path starts from the root directory (`/`) and goes through every intermediate directory (`home`, `user`, `Documents`) until it reaches the file (`file.txt`).

On the other hand, a relative file path is a file path that starts from the current working directory. For example, if the current working directory is `/home/user/Documents`, a relative file path to a file in the same directory might look like `file.txt`, whereas a relative file path to a file in the parent directory might look like `../otherfile.txt`.

Section 2: Changing the current working directory with os.chdir()

In order to open a file in a relative location in Python, we first need to make sure that the current working directory is set to the correct directory. We can do this using the `os.chdir()` function.

`os.chdir()` takes one argument, which is the absolute or relative file path to the directory we want to change to. For example, if we want to change the current working directory to `/home/user/Documents`, we can use `os.chdir('/home/user/Documents')`. If we want to change the current working directory to a directory that is located relative to the current working directory, we can use a relative file path instead of an absolute file path.

Section 3: Opening a file in a relative location with open()

Once we have changed the current working directory to the directory where our file is located, we can open the file using the `open()` function. 

To open a file in Python, we need to specify the file name and the mode we want to open the file in. For example, to open a file called `file.txt` for reading, we can use `open('file.txt', 'r')`. 

If the file is located in the current working directory, we can refer to the file using just its name. If the file is located in a subdirectory, we can use a relative file path to refer to it. For example, if the file is located in the `data` subdirectory, we can use `open('data/file.txt', 'r')` to open it.

Section 4: Putting it all together: an example

Here is an example of how to open a file in a relative location in Python:

```
import os

# Change the current working directory to the directory where the file is located
os.chdir('/home/user/Documents/data')

# Open the file for reading
with open('file.txt', 'r') as f:
    # Read the contents of the file
    contents = f.read()
    print(contents)
```

In this example, we first change the current working directory to `/home/user/Documents/data`. Then we open the file `file.txt` for reading using `open('file.txt', 'r')`. Finally, we read the contents of the file using the `read()` method and print them to the console.
