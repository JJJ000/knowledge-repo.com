---
title: What is the command to find the width of a linux console window using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Linux console window width can be retrieved in Python using the os.get\_terminal\_size() method.
---

**Contents**

[TOC]

# Section 1: Using the Linux Terminal

The width of a Linux console window can be obtained by using the `stty size` command. This command will output the width and height of the terminal window in the following format: `rows columns`. The width of the window is the second value in the output.

# Section 2: Using Python

The width of a Linux console window can be obtained in Python by using the `os.popen()` function. This function takes a command as a parameter and returns the output of the command as a file object. To obtain the width of the terminal window, the `stty size` command is passed to this function and the output is parsed to get the width.

# Section 3: Example Code

The following code snippet shows how the width of a Linux console window can be obtained in Python:

```
import os

# Get the output of the stty size command
output = os.popen('stty size').read()

# Split the output into rows and columns
rows, columns = output.split()

# Print the width of the terminal window
print(columns)
```

# Section 4: Output

The output of the code snippet above will be the width of the terminal window in characters.
