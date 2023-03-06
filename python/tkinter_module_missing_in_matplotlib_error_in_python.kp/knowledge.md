---
title: The error message 'no module named tkinter' appears while using matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The tkinter module needs to be installed separately as it is not included in the default Python installation.
---

**Contents**

[TOC]

Section 1: Explanation of the error
The "no module named tkinter" error in matplotlib indicates that Python's tkinter module is either missing or corrupt on the system. This error usually occurs when using Python 2.x versions since tkinter is a default module in Python 3.x versions.

Section 2: Solution for Windows
To fix the issue on Windows, follow the steps below:

1. Install the latest version of Python on the system.
2. During the installation process, make sure to select the "Add Python X to PATH" checkbox to include Python to the environment variables.
3. Open Command Prompt and install tkinter using the following command:
   ```
   pip install python-tk
   ```
4. Once the installation is complete, try running the matplotlib script again.

Section 3: Solution for Linux
To fix the issue on Linux, follow the steps below:

1. Install tkinter and related dependencies by running the following command:
   ```
   sudo apt-get install python3-tk
   ```
2. Once the installation is complete, try running the matplotlib script again.

Section 4: Solution for macOS
To fix the issue on macOS, follow the steps below:

1. Install the latest version of Python on the system.
2. Install tkinter using the following command:
   ```
   brew install python-tk@3.x
   ```
   Replace "x" with the specific version of Python installed on the system.
3. Once the installation is complete, try running the matplotlib script again.
