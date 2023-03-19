---
title: How to open a document using the default operating system application in python, for both windows and mac os?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `os.startfile()` function in Windows and the `subprocess.run()` function in Mac OS to open a document with the default OS application.
---

**Contents**

[TOC]

Section 1: Background
When working with files, it is often necessary to open them using the default application installed in the operating system. For example, opening a PDF file with the default PDF viewer. Python provides a way to achieve this functionality regardless of which operating system the code is running on.

Section 2: Opening documents in Windows
The os module in Python can be used to open a file in the default application in Windows using the startfile() method. This method opens a file with its associated application, similar to double-clicking on the file in the File Explorer.

Here is an example code for opening a PDF file in Windows:

import os
os.startfile("C:/Users/User/Documents/sample.pdf")

The above code will open the sample.pdf file in the default PDF viewer installed in the system.

Section 3: Opening documents in Mac OS
On Mac OS, the subprocess module can be used to open a file in the default application. The open command with the -a flag is used to open the file in the default application.

Here is an example code for opening a PDF file in Mac OS:

import subprocess
subprocess.call(('open', '/Users/user/Documents/sample.pdf'))

The above code will open the sample.pdf file in the default PDF viewer on Mac OS.

Section 4: Conclusion
In conclusion, opening documents with the default system application can be done using Python in both Windows and Mac OS. The startfile() method from the os module is used for Windows, while the subprocess module is used for Mac OS. This functionality can be useful in many applications where users need to view or edit files without leaving the application.
