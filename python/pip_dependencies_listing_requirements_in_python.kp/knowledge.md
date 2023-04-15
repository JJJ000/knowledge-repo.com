---
title: Can pip dependencies or requirements be listed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can list pip dependencies/requirements in Python using the command `pip freeze`.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, dependencies or requirements of a project can be managed using pip, the package installer for Python. Pip can install and manage software packages with dependencies automatically. It is essential to keep track of the dependencies when working on a project, as it helps to maintain the compatibility of the code.

Section 2: Viewing installed packages
To view the list of installed packages along with their version, use the following command in the terminal or command prompt:
```
pip freeze
```
The command will display the package name and version number in the format required by pip for installation.

Section 3: Saving dependencies to a file
To save dependencies to a file, use the following command:
```
pip freeze > requirements.txt
```
The command will save the list of packages and their versions to a file named requirements.txt in the current directory. This file can be committed to the version control system for sharing with others.

Section 4: Installing dependencies from a file
To install dependencies from a file, use the following command:
```
pip install -r requirements.txt
```
The command will install the packages and their dependencies listed in the requirements.txt file.

In conclusion, managing dependencies is essential for maintaining the functionality and compatibility of a Python project. By using pip, Python developers can easily list, save, and install the required packages and their dependencies.
