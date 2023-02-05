---
title: What is the process for executing Python code using sublime text 2?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To run Python code from Sublime Text 2, press Ctrl+B (on Windows) or Cmd+B (on macOS).
---

**Contents**

[TOC]

# Step 1: Install Package Control
Sublime Text 2 does not come with a built-in interpreter for Python. To run Python code, you must install a package that provides this functionality. The easiest way to do this is by using Package Control.

# Step 2: Install Python-Specific Packages
Once Package Control is installed, you can open the Command Palette (Ctrl+Shift+P) and type “install” to bring up the Package Control: Install Package option. From there, you can search for and install packages that provide Python-specific functionality, such as SublimeREPL or SublimePythonIDE.

# Step 3: Configure the Packages
Once the packages are installed, you will need to configure them to work with your Python interpreter. Depending on the package you have installed, this may involve setting the path to your Python interpreter in the package settings.

# Step 4: Run the Code
Once the packages are configured, you can open a Python file in Sublime Text 2 and run it by selecting the appropriate command from the Command Palette. For example, if you have installed SublimeREPL, you can select the “SublimeREPL: Python - RUN current file” command to run the code in the current file.
