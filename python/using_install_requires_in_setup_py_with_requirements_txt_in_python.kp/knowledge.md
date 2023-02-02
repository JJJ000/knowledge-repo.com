---
title: Consult requirements.txt for the list of packages to include in the install_requires argument of setuptools setup.py file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Requirements.txt is a text file that contains a list of all the packages and their versions that are required for the project to run.
---

**Contents**

[TOC]

# Overview

The requirements.txt file is used in the setuptools setup.py file to specify the packages and versions that should be installed when a user runs the setup.py file. The install_requires kwarg is used in the setup.py file to specify the list of packages and versions that should be installed.

# Syntax

The install_requires kwarg is a list of strings in the form of 'package_name>=version'. For example:

install_requires=['requests>=2.20.0', 'numpy>=1.14.0']

# Requirements.txt

The requirements.txt file is used to specify the packages and versions that should be installed when a user runs the setup.py file. The format of the file is a list of strings in the form of 'package_name>=version'. For example:

requests>=2.20.0
numpy>=1.14.0

# Usage

The install_requires kwarg in the setup.py file should be set to the contents of the requirements.txt file. For example:

install_requires=open('requirements.txt').read().splitlines()
