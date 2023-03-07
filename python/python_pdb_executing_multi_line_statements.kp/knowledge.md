---
title: What is the method for running multi-line statements within python's built-in debugger (pdb)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `!` (exclamation) symbol followed by the desired multi-line code block enclosed in triple quotes.
---

**Contents**

[TOC]

1. Introduction to PDB
Python's debugger, PDB, is a powerful tool for debugging code. It allows you to control the execution of your code line by line, inspecting variables and functions at each step. One common use case for PDB is to debug code that has errors, such as syntax errors or logic errors.

2. Entering PDB mode
To enter PDB mode, you can add the following line of code to your Python script:
```
import pdb; pdb.set_trace()
```
When the interpreter encounters this line, it will pause the execution of the script and drop you into the PDB shell. From here, you can interact with your code line by line.

3. Executing multi-line statements
To execute multi-line statements within PDB, you'll need to use the `!` command. This command tells PDB to execute the following statement as a Python command, rather than a PDB command.

For example, let's say you have the following multi-line statement in your code:
```
x = 1 + 2 + \
    3 + 4 + \
    5 + 6
```
If you try to execute this line within PDB using the `next` command, you'll get a syntax error. To execute it correctly, you can use the following command in PDB:
```
!x = 1 + 2 + \
    3 + 4 + \
    5 + 6
```
This tells PDB to execute the multi-line statement as a Python command, rather than trying to interpret it as a series of PDB commands.

4. Conclusion
In summary, you can use Python's debugger, PDB, to control the execution of your code line by line and inspect variables and functions at each step. To execute multi-line statements within PDB, you'll need to use the `!` command to tell PDB to execute the statement as a Python command. With these tools, you can effectively debug your code and fix errors quickly and efficiently.
