---
title: What is the method of incorporating package data using setuptools/distutils?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Include package data in the setup() function of setup.py using the package\_data parameter.
---

**Contents**

[TOC]

## Overview

When distributing a package in Python, there may be additional files or data that needs to be included with the package. Examples of these files could be configuration files, examples, or resources such as images or templates. With `setuptools` or `distutils`, it is possible to include additional data files or folders with the package distribution. This can be done by specifying which files or folders need to be included with the package in the `setup.py` file.

## Using data_files option

One way to include additional data with the package is to use the `data_files` option in the `setup` function. This option accepts a list of tuples, where each tuple contains two elements. The first element is the destination directory where the data should be installed, relative to the installation prefix. The second element is a list of files or directories to include. For example:

```python
from setuptools import setup

setup(
   # other arguments ...
   data_files=[('my_package/data', ['data/example.txt', 'data/example2.txt'])]
)
```

In this example, the files `example.txt` and `example2.txt` located in the `data` directory are included with the package in a new `data` directory relative to the installation prefix.

## Using package_data option

Another way to include additional data with the package is to use the `package_data` option in the `setup` function. This option takes a dictionary where the keys are package names and the values are lists of relative file paths to include. For example:

```python
from setuptools import setup

setup(
   # other arguments ...
   package_data={'my_package': ['data/*.txt']}
)
```

In this example, all `.txt` files located in the `data` directory inside the `my_package` package are included with the distribution.

## Including data inside the package directory

A third option is to include data files inside the package directory using a package-relative path. This can be done by including the data files inside the package directory and specifying their relative path in the `setup.py` file using the `setuptools.find_packages` function.

For example, if the package directory structure is as follows:

```
my_package/
   __init__.py
   data/
      example.txt
   module/
      __init__.py
      foo.py
```

Then the `setup.py` file can be written as follows:

```python
from setuptools import setup, find_packages

setup(
   # other arguments ...
   packages=find_packages(),
   include_package_data=True
)
```

In this example, the `find_packages` function is used to automatically discover packages and dependencies, and the `include_package_data` option is set to `True` to include all files specified in the `MANIFEST.in` file in the package distribution. The `MANIFEST.in` file should include the following line:

```
include my_package/data/*
```

This will include the `example.txt` file located in `my_package/data` with the package distribution. The package data can be accessed using the `pkg_resources` module:

```python
import pkg_resources

data = pkg_resources.resource_string(__name__, 'data/example.txt')
```

## Conclusion

In this article, we have seen three ways in which additional data can be included with a package distribution using `setuptools` or `distutils`. By using the `data_files` option, the `package_data` option, or including data inside the package directory using a package-relative path, the package distribution can include all of the necessary files and data for a successful installation.
