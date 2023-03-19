---
title: For what purpose is the "--no-cache-dir" option in pip used?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The `--no-cache-dir` option in pip is used to prevent caching of package installation information and files, and ensure that the latest version of a package is installed every time.
---

**Contents**

[TOC]

### Introduction

Pip is a Python package manager. It is used to download and install Python modules, libraries, and frameworks. Pip comes with various options that you can use to customize the installation process. One of these options is `--no-cache-dir`.

### Caching

When you install a package using Pip, it downloads the package from PyPI (Python Package Index) and installs it on your system. Pip stores the downloaded packages in a cache directory, which speeds up future installations of the same package. 

### No-cache-dir

The `--no-cache-dir` option tells Pip to skip the cache directory and download the package every time you install it. This can be useful when you want to make sure that you are installing the latest version of a package or if you are having issues with the cache directory.

### When to use it

There are a few scenarios where `--no-cache-dir` could be useful:

1. If you are having issues with the cache directory, such as permissions or disk space problems.

2. If you want to make sure that you are installing the latest version of a package.

3. If you are using a shared machine and don't have write access to the cache directory. 

Overall, `--no-cache-dir` is a useful option to have in your Pip toolbox, but you should use it sparingly, as it can slow down your installation process by downloading the package every time.
