---
title: Construct the complete file path name using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The full path filename in Python can be built using the os.path.join() function.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, we can build the full path filename by using the `os.path` module. This module provides a variety of functions for working with file paths, including joining paths together to create the full path filename.

## Section 2: Using os.path.join()
The `os.path.join()` function is used to join two or more file path components into a single path. The function takes two or more arguments, where each argument is a file path component. The function returns a string that represents the full path filename created by joining the supplied path components.

Here's an example usage of `os.path.join()` to build a full path filename:

```
import os

directory = "/path/to/dir"
filename = "file.txt"

# join the directory and filename to create the full path filename
full_path = os.path.join(directory, filename)

print(full_path) # output: "/path/to/dir/file.txt"
```

In this example, we create two variables `directory` and `filename` that represent the directory and filename components of the full path filename, respectively. We use `os.path.join()` to join these components together into a single string, which is then assigned to the `full_path` variable.

## Section 3: Using string concatenation
Another way to build a full path filename in Python is to use string concatenation. This method involves concatenating the directory and filename strings together, using a separator character such as "/".

Here's an example usage of string concatenation to build a full path filename:

```
directory = "/path/to/dir"
filename = "file.txt"

# concatenate the directory and filename to create the full path filename
full_path = directory + "/" + filename

print(full_path) # output: "/path/to/dir/file.txt"
```

In this example, we create two variables `directory` and `filename` that represent the directory and filename components of the full path filename, respectively. We then use string concatenation to join these components together, using the "/" character to separate them.

## Section 4: Conclusion
In conclusion, Python provides two main methods for building full path filenames: using `os.path.join()` or string concatenation. Both methods are effective and reliable, and the choice of method depends on personal preference and coding style. By using these methods, we can easily create full path filenames that can be used to interact with files and directories in our programs.
