---
title: Why is distutils still in use despite the availability of setuptools?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Distutils is still a thing in Python because it is part of the standard library and provides basic functionality for packaging and distributing Python modules, while setuptools offers more advanced features and is not included in the standard library.
---

**Contents**

[TOC]

Overview
----------
Python is a widely-used programming language, and in order to distribute packages, it has two main library technologies: distutils and setuptools. Both of these tools facilitate the distribution of Python packages, but they have several differences. In this article, we will discuss why distutils is still a thing in Python and why it is still used.

What is distutils?
----------
Distutils is the original packaging system for Python. It is used to build, distribute, and install Python modules. It is a part of the Python standard library, which means that it comes with every Python distribution. Distutils allows developers to create modules, packages, and distribution packages for Python.

What is setuptools?
----------
Setuptools is an open-source package that is used to manage and distribute Python packages. It is a third-party package that was created to extend the functionality of distutils. Setuptools provides features such as automatic egg creation, easy installation of dependencies, and package discovery. It is written in Python and uses distutils to build and distribute Python packages.

Why distutils is still a thing in Python?
----------
Distutils is still a thing in Python for several reasons. Firstly, it is included in the standard library of Python which means it can be used out of the box. Secondly, it is simple and easy to use. Distutils has a minimalistic API which makes it easy for developers to start creating simple packages without a steep learning curve. Finally, distutils is still used because different operating systems might have different versions of Python, so using a standard packaging system ensures that the packages can be executed on almost any platform where Python is installed.

Conclusion
----------
Distutils and setuptools are both good tools for building and distributing Python packages. While setuptools provides more features than distutils, distutils is still a thing in Python since it is a part of the Python standard library, easy to use, and cross-platform. However, if a developer wants to take full advantage of Python's package management system, then using setuptools is recommended as it includes more features than distutils.
