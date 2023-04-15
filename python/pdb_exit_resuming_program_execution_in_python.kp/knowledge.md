---
title: What is the method to leave pdb and permit the program to proceed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Type `continue` in the pdb console and press enter to allow the program to continue.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, debugging is an essential part of writing code. The Python debugger called pdb allows developers to step through their code and identify bugs. However, once a bug is identified and fixed, the developer needs to exit pdb and allow the program to continue executing normally. This article explains how to exit pdb and resume the execution of the code.

Section 2: Exiting pdb
To exit pdb and allow the program to continue, you can use the command `q` in the pdb prompt. This command stands for “quit,” and it will take you out of the debugger and return you to the Python shell. Once you execute this command, the program will continue running normally until completion or until it encounters another breakpoint.

Section 3: Exiting pdb without quitting
If you want to exit pdb without quitting the program altogether, you can use the command `c` instead. This command stands for “continue,” and it will let the program continue running until it encounters another breakpoint or until it finishes.

Section 4: Conclusion
The pdb debugger is a powerful tool for identifying and fixing bugs in Python programs. However, it’s essential to know how to exit pdb and allow the program to continue running normally. Using the `q` or `c` command in the pdb prompt can achieve this. By mastering pdb and other debugging tools, developers can improve the quality of their code and build more robust software.
