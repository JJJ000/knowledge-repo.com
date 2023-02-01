---
title: What are the distinctions between distribute, distutils, setuptools and distutils2?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Distribute is a fork of Setuptools, while Distutils and Distutils2 are both standard library packages that provide a framework for packaging and distributing Python code.
---

**Contents**

[TOC]

#Distribute
Distribute is a fork of the original setuptools project. It was created to address various issues with the original setuptools project, such as its lack of support for Python 3 and its slow development process. It was initially released in 2009 and is now the most widely used packaging system for Python.

#Distutils
Distutils is the original packaging system for Python. It was first released in 1998 and is now considered deprecated. It does not support Python 3 and has a much more limited feature set than setuptools or distribute.

#Setuptools
Setuptools is a fork of the original Distutils project. It was created to address the shortcomings of the original Distutils project. It was first released in 2004 and is now the most widely used packaging system for Python. It supports Python 2 and Python 3 and has a much more comprehensive feature set than Distutils.

#Distutils2
Distutils2 is a fork of the original Distutils project. It was created to address the shortcomings of the original Distutils project. It was first released in 2011 and is now considered deprecated. It supports Python 2 and Python 3 and has a much more comprehensive feature set than Distutils, but it is not as widely used as setuptools or distribute.
