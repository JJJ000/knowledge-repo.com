---
title: Locate the installation directory of python, in case it is not in the default path
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The path where Python is installed can be found by running the command `which python` in the terminal/cmd prompt.
---

**Contents**

[TOC]

## Option 1: Using the command line

1. Open a terminal or command prompt.
2. Type `python` and press enter.
3. If Python is installed, it should launch the Python interpreter and display the version number.
4. Type `import sys` and press enter.
5. Type `print(sys.executable)` and press enter.
6. The output should be the path to the Python executable.


## Option 2: Checking environment variables

1. Open a terminal or command prompt.
2. Type `echo %PATH%` (Windows) or `echo $PATH` (Mac/Linux) and press enter.
3. This will display a list of directories separated by semicolons (Windows) or colons (Mac/Linux) that are included in your system's PATH environment variable.
4. Look for a directory that contains the Python executable. This could be the default installation directory, or another directory that you or your system administrator configured.
5. Once you locate the directory, you can navigate to it using the command line or file explorer to find the Python installation.


## Option 3: Searching the file system

1. Open a file explorer or Finder window.
2. Navigate to the root directory (Windows: `C:\`, Mac/Linux: `/`).
3. In the search bar, type `python`.
4. This should display a list of all files and directories containing "python" in the name or file path.
5. Look for folders or files that suggest a Python installation, such as `Python`, `Anaconda`, or `Miniconda`.
6. Once you locate the directory, you can navigate to it using the file explorer or command line to find the Python installation.


## Option 4: Checking documentation or installation notes

1. If Python was installed by your system administrator or IT department, they may have provided documentation or installation notes that specify the installation directory.
2. Check any documentation or notes related to the Python installation to see if the installation directory is listed.
3. If you installed Python yourself, check any installation instructions or notes that you saved or bookmarked during the installation process.
4. You may also be able to find installation notes or documentation online from the website or source where you downloaded Python.
