---
title: In what situations is the pip install option of -e, --editable beneficial?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The -e, --editable option would be useful when developing a package and testing it in a local environment without the need to constantly reinstall it.
---

**Contents**

[TOC]

# Introduction

pip is a package manager for Python. It is used to install and manage software packages written in Python. The -e, --editable option is used with pip install to install packages in "editable" mode. In this mode, the package is installed as a symbolic link to the source code directory. 

# Useful in Development

The -e, --editable option is most useful in development scenarios. When developers are working on a package and want to install it in a way that any changes they make to the package code are immediately reflected in the installed version, they would use the -e option. 

For example, a developer may work on a Django project and want to install a custom Django package they are developing so that any changes they make to the package code will be immediately reflected in the installed version. In this case, they would use the -e option with pip install to install the package in editable mode.

# Allows Testing of Unpublished Code

Using the -e option also allows developers to test their unpublished code against other packages they are working on. For example, a developer may be working on two related packages, one of which depends on the other. By installing the packages in editable mode and modifying the code of one package, they can test how changes to one package affect the other. 

# Facilitates Collaboration

The -e option also facilitates collaboration among developers. By installing packages in editable mode, developers can work collaboratively on a project, each working on their own copy of the source code, and have changes immediately reflected in the installed version of the package. 

This makes it easier for developers to work together on large projects, where packages may have many dependencies, and changes to one package may affect many other packages.

# Conclusion

In summary, the -e, --editable option is useful when developers want to install packages in "editable" mode so that changes to the package source code are immediately reflected in the installed version. This mode is most useful in development scenarios, enables testing of unpublished code, and facilitates collaboration among developers.
