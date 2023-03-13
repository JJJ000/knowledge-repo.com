---
title: Could you explain the purpose of "pip install -e"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: `pip install -e` is used to install a Python package in `editable` mode, allowing developers to continuously make changes to the code without having to reinstall it each time.
---

**Contents**

[TOC]

### Introduction
`pip install -e` is a command used in Python to install a package in editable mode from a local directory or a version control system link such as Git. In this mode, changes made to the local package are immediately reflected in the installed package. The use cases for `pip install -e` are numerous.

### Developing a Python Package
Developers use the `-e` option when working on a Python package to make changes and test them immediately without having to reinstall the package frequently. They can edit the code locally in their development environment and test them instantly without having to rebuild or reinstall the package. 

Another advantage of using the editable mode is that developers can work on multiple versions of the same package and test their compatibility with their Python application. This flexibility is particularly important when working on large projects that require multiple contributors to the same codebase.

### Installing Dependencies
Another use case for `pip install -e` is when working with packages that depend on other packages. Using the editable mode allows developers to install all dependencies in one command, without having to worry about version incompatibilities or other issues that may arise from installing packages individually.

### Contributing to Open Source Projects
For contributors to open source projects, `pip install -e` provides an easy way to get started with the project by allowing them to make changes and test them in real-time. It eliminates the need to clone and set up the project locally or go through the hassle of building and installing the package. 

Contributors can install the package in editable mode, create a branch of the package and make changes to it, submit a pull request and have the changes reviewed and accepted without having to reinstall or modify the package.

### Conclusion
In summary, `pip install -e` is a powerful command that developers use for flexible, easier and faster development of Python packages. It allows for real-time changes and supports collaboration, testing, and developing dependencies.
