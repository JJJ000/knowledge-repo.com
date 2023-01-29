---
title: What is the best way to read the contents of a file into a list, line-by-line?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `for line in open(filename)` syntax to read a file line-by-line into a list in Python.
---

**Contents**

[TOC]

##### Section 1: Import the Necessary Modules

Before you can read a file line-by-line, you must first import the necessary modules. The most common modules used for reading files in Python are the `open` and `readline` modules.

```
import open
import readline
```

##### Section 2: Open the File

Once the necessary modules have been imported, you can open the file. To do this, you must specify the file path and the mode. The mode can be either `'r'` for reading or `'w'` for writing.

```
file_path = "/path/to/file.txt"
file = open(file_path, "r")
```

##### Section 3: Read the File Line-by-Line

Now that the file has been opened, you can begin reading it line-by-line. To do this, you must use the `readline()` method. This method will read one line at a time and return it as a string.

```
line = file.readline()
```

##### Section 4: Append the Lines to a List

Once the line has been read, you can append it to a list. To do this, you must use the `append()` method.

```
lines = []
while line:
    lines.append(line)
    line = file.readline()
```

Once the `while` loop has finished executing, the `lines` list will contain all of the lines from the file.
