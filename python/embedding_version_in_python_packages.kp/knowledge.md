---
title: What is the typical method for including version information in a Python package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The recommended way to embed version information into a Python package is to include a version.py module containing version information.
---

**Contents**

[TOC]

# Version Identification

When packaging a Python project, it is important to include a version identifier. This allows users to quickly identify the version of the package they are using, as well as to track changes and bug fixes over time.

# Version Format

The version identifier should follow the Semantic Versioning (SemVer) standard. This format consists of three numbers separated by periods, such as `1.2.3`. The first number is the major version, the second is the minor version, and the third is the patch version.

# Versioning in Python

The Python Packaging Authority (PyPA) recommends using the `packaging` library to manage versioning. This library provides a `Version` class that can be used to represent a version identifier. The `packaging` library also provides functions for parsing and comparing versions.

# Version in Setup

The version should also be included in the `setup.py` file. This allows users to easily identify the version of the package they are installing. The version can be specified using the `version` argument in the `setup()` function.
