---
title: How can I run a file using the Python interpreter?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can execute a file within the Python interpreter by using the exec() function.
---

**Contents**

[TOC]

# Step 1: Locate File

The first step is to locate the file you wish to execute. It is important to note the full path of the file, as this is what will be used to execute the file.

# Step 2: Open Python Interpreter

Once the file has been located, open the Python interpreter. This can be done by opening the command line and typing in `python`.

# Step 3: Execute File

Once the Python interpreter is open, type in the command `exec(open('path/to/file.py').read())`, replacing `path/to/file.py` with the full path of the file you wish to execute.

# Step 4: Output

Once the command is executed, the output of the file will be displayed.
