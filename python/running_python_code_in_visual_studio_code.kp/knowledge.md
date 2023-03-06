---
title: What is the method of running Python code in visual studio code?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To execute Python code from within Visual Studio Code, press F5 or choose Run from the Run menu and select the Python file you want to execute.
---

**Contents**

[TOC]

# Installing the Python extension

1. Open Visual Studio Code and click on the Extensions icon on the left hand side of the screen (or press Ctrl+Shift+X).
2. Search for "Python" in the search bar and click on the install button next to the "Microsoft Python extension".
3. Wait for the extension to install and then restart Visual Studio Code.

# Creating a Python file

1. Click on the File menu at the top of the screen and select New File (or press Ctrl+N).
2. Type out your Python code in the new file.
3. Save the file with a .py extension (e.g. "myfile.py") by clicking on the File menu and selecting Save As (or press Ctrl+Shift+S).

# Running the Python code

1. Open the Python file you want to run in Visual Studio Code.
2. Click on the Run menu at the top of the screen and select Run Without Debugging (or press Ctrl+F5).
3. Visual Studio Code will now run your Python code and display the output in the terminal window at the bottom of the screen.

# Debugging the Python code

1. Open the Python file you want to debug in Visual Studio Code.
2. Click on the Debug menu at the top of the screen and select Add Configuration.
3. Select the "Python: Current File" option and save the configuration.
4. Add breakpoints in your code by clicking on the line number on the left hand side of the code editor.
5. Click on the Run menu at the top of the screen and select Start Debugging (or press F5).
6. Visual Studio Code will now run your Python code in debug mode and stop at any breakpoints you added. You can then step through the code and inspect variables as needed.
