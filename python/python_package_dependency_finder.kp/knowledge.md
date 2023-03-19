---
title: What are the steps to determine the dependencies of a Python package?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the command `pip show <package\_name>` to view a package`s metadata, including its dependencies.
---

**Contents**

[TOC]

## Introduction

When working with Python, you may encounter situations where you need to find the dependencies of a particular package. Dependencies are other packages that are required for the package to run properly. In this tutorial, we will explore different ways to find the dependencies of a Python package.


## Using pip command

One of the easiest and most common ways to find a package's dependencies is by using the `pip` command with the `show` option. Open up your command prompt and enter the following command:

```
pip show <package_name>
```

This will output information about the package, including its dependencies. Look for the `Requires` line in the output, which will list the package's dependencies.


## Using pipdeptree module

Another way to find dependencies is by using the `pipdeptree` module. This module provides a tree-like visual representation of a package's dependencies. To use this module, install it using pip:

```
pip install pipdeptree
```

Then, run the following command:

```
pipdeptree
```

This will output a tree diagram of all the packages installed on your system, and their dependencies. You can also specify a specific package by running:

```
pipdeptree <package_name>
```


## Using PyPI website

If you don't have access to the command line or would like a more user-friendly interface, you can use the Python Package Index (PyPI) website. Simply open up your web browser and navigate to:

```
https://pypi.org/project/<package_name>/
```

Replace `<package_name>` with the name of the package you want to find the dependencies for. On the package's PyPI page, look for the `Requires` section, which will list the package's dependencies.


## Conclusion

In this tutorial, we explored different ways to find the dependencies of a Python package. Whether you prefer using the command line with `pip`, a module like `pipdeptree`, or a web browser with PyPI, there are several methods available for finding a package's dependencies.
