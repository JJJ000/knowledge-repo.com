---
title: Bringing in files from another directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the `os.path.join` function to import files from different folders in Python.
---

**Contents**

[TOC]

# 1. Set Path

In order to import files from a different folder in Python, the first step is to set the path. This can be done by using the os.chdir() function, which changes the current working directory of the program.

# 2. Import File

Once the path has been set, the file can be imported using the open() function. The open() function takes in two parameters: the file name and the mode. The mode parameter specifies the mode of the file, such as read-only, write-only, or append.

# 3. Read File

Once the file has been imported, it can be read using the read() function. The read() function takes in one parameter, which is the number of characters to be read. The read() function returns a string containing the characters read from the file.

# 4. Close File

Finally, the file should be closed when it is no longer needed. This can be done using the close() function. The close() function takes in no parameters and returns nothing.
