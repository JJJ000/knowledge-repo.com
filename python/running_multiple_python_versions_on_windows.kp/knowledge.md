---
title: What are the steps to use multiple Python versions on windows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a virtual environment or a separate installation for each Python version.
---

**Contents**

[TOC]

# Introduction
Python is a popular programming language used for developing countless applications. However, sometimes you might need to work with different versions of Python on the same machine. This could be because different projects demand different versions, or because you want to test your code on different versions. In this tutorial, we'll discuss the various ways to run multiple Python versions on Windows. 

# Method 1: Using Python Launcher
Python Launcher is a tool that enables you to run multiple versions of Python on the same machine. Here's how you can use it:

1. Install the latest versions of both Python 2 and Python 3 on your machine. During the installation, make sure to check the box that says "Add Python to PATH."
2. Open a new Command Prompt window and type "py --version". This should display the latest version of Python installed on your machine.
3. To specify which version of Python you want to run, use the following command: "py -[version number] [script.py]". For example, if you want to run a script using Python 3.7, type "py -3.7 file.py" in the command prompt. 

# Method 2: Using Anaconda
Anaconda is a popular distribution of Python used for data science and machine learning. It allows you to create multiple environments with different versions of Python and packages. Here's how to use it:

1. Download and install Anaconda on your machine.
2. Open the Anaconda Command Prompt from the start menu.
3. To create an environment with a specific version of Python, type "conda create --name [name of environment] python=[version number]". For example, to create an environment with Python 3.7, type "conda create --name env37 python=3.7".
4. Activate the environment using the command "conda activate [name of environment]".
5. You can now install packages within this environment using "conda install [package name]". 

# Conclusion
These are two simple methods to run multiple versions of Python on your Windows machine. Python Launcher is the easiest way to quickly switch between different versions, while Anaconda provides a more comprehensive solution for working with different Python environments. Choose the one that suits your use case and start working with multiple versions of Python today!
