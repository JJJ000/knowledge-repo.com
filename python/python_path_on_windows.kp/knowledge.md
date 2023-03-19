---
title: How to include Python in path in windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To add Python to PATH on Windows, go to system properties -> Environment Variables -> edit the PATH variable and add the Python installation path.
---

**Contents**

[TOC]

# Introduction

Python is a popular programming language used for developing applications, web development, data analysis, automation, and much more. If you are a Windows user, it is necessary to add Python to the PATH environment variable to use it from the Command Prompt. In this tutorial, we will discuss how to add Python to PATH on Windows.

# Finding the Python installation directory

Before adding Python to PATH, we need to first find the directory where Python is installed. To find the location of the Python installation directory, follow these steps.

1. Open the File Explorer on your Windows machine.
2. Navigate to the directory where you have installed Python. By default, Python is installed in the `C:\Users\Username\AppData\Local\Programs\Python` directory.

# Adding Python to PATH

Once you have located the Python installation directory, follow these steps to add Python to PATH.

1. Open the Start menu and search for "Environment Variables". Select "Edit the system environment variables" from the search results.
2. In the "System Properties" window, click the "Environment Variables" button.
3. Under the "System Variables" section, scroll down and select the "Path" variable. Click the "Edit" button to edit the variable.
4. In the "Edit environment variable" window, click the "New" button and enter the path to the Python installation directory. For example, if you have installed Python 3.8 in the `C:\Users\Username\AppData\Local\Programs\Python\Python38` directory, you should add `C:\Users\Username\AppData\Local\Programs\Python\Python38` to the PATH variable.
5. Click "OK" on all the open windows to save the changes.

# Verifying Python installation

To verify that Python has been added to PATH successfully, open the Command Prompt and type `python --version`. If you see the Python version number displayed on the screen, it means Python has been added to PATH successfully.

# Conclusion

In this tutorial, we have discussed how to add Python to PATH on Windows. Adding Python to PATH is essential if you want to use it from the Command Prompt to execute Python scripts or run Python commands.
