---
title: Find and replace a line in a file using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the replace() method of the file object to search and replace a line in a file in Python.
---

**Contents**

[TOC]

# Section 1: Opening the File

In order to search and replace a line in a file in Python, the file must be opened first. This can be done using the `open()` function. The syntax for this function is `open(file, mode)`, where `file` is the path to the file and `mode` is the mode used to open the file. The mode should be set to `'r+'` to open the file in read and write mode.

# Section 2: Reading the File

Once the file is opened, it can be read line by line using a for loop. The syntax for this loop is `for line in file:`, where `file` is the file object returned by `open()`. This loop will iterate over each line in the file and store it in the `line` variable.

# Section 3: Replacing the Line

Once the line to be replaced is read, it can be replaced by using the `replace()` method. The syntax for this method is `line.replace(old, new)`, where `old` is the string to be replaced and `new` is the string to replace it with.

# Section 4: Writing the File

Finally, the modified line can be written back to the file using the `write()` method. The syntax for this method is `file.write(line)`, where `file` is the file object returned by `open()` and `line` is the modified line.
