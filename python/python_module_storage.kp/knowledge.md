---
title: In which location are the Python modules stored?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python modules are stored in various directories depending on the installation, operating system, and user settings, but can be accessed using the `sys.path` list.
---

**Contents**

[TOC]

## Introduction

Python modules are an essential part of the Python language, providing additional functionality to programmers. When a module is imported, Python looks for it in a set of directories, known as the "search path". In this article, we will explore where the Python modules are stored.


## Built-In Modules

Python comes with a set of built-in modules that provide functionality for performing various tasks. These modules are installed with the Python interpreter and are stored in the lib directory of the Python installation.

For example, the math module is a built-in module that provides mathematical operations and functions. It is stored in the following directory:

```
/usr/lib/python3.8/
```


## User-Installed Modules

Python programmers often use third-party libraries to extend the functionality of their applications. These libraries come in the form of Python modules and need to be installed on the system before they can be used.

User-installed modules are stored in several locations on the system, depending on the method used to install them. The most common locations for user-installed modules are:

- Site-packages directory: This is a directory that contains all the user-installed modules that are available to all users on the system. It is usually located in the lib directory of the Python installation.

- Virtual environment directory: A virtual environment is a method of creating an isolated Python environment for a specific application. User-installed modules are stored in the site-packages directory of the virtual environment.

For example, if we install the requests library using pip, it will be stored in one of the following directories:

```
/usr/lib/python3.8/site-packages/
/home/user/myproject/venv/lib/python3.8/site-packages/
```


## Conclusion

In summary, Python modules are stored in various locations on the system, depending on whether they are built-in or user-installed. Built-in modules are stored in the lib directory of the Python installation, while user-installed modules can be stored in the site-packages directory or the site-packages directory of a virtual environment.
