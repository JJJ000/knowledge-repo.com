---
title: What is the reason for Python setup.py displaying an invalid command 'bdist_wheel' when running on travis ci?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The `bdist\_wheel` command is not supported by the version of Python being used on Travis CI.
---

**Contents**

[TOC]

# Overview 
Python setup.py is a script used to build and install Python packages. The 'bdist_wheel' command is an optional command used to create a wheel package, which is a type of built package used for distribution. When running setup.py on Travis CI, this command may fail due to an incompatibility between the wheel package and the Travis CI environment.

# What is a Wheel Package?
A wheel package is a built distribution format for Python packages. It is a built package that can be installed easily on any platform, and it is the preferred way to install Python packages. Wheels are built from source distributions, which are archives of files that contain the project source code and metadata.

# Why Does 'bdist_wheel' Fail on Travis CI?
The wheel package is not compatible with the Travis CI environment, so when the 'bdist_wheel' command is run, it fails. This is due to the fact that Travis CI does not have the necessary tools to build wheel packages. 

# How to Resolve This Issue
The best way to resolve this issue is to use an alternative method to build and install the Python package. This can be done by using the 'install' command instead of the 'bdist_wheel' command. The 'install' command will install the package directly from the source distribution, without creating a wheel package.
