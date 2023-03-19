---
title: Adding non-python files using setup.py
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To include non-Python files with setup.py, use the `package\_data` or `data\_files` argument in the `setup()` function.
---

**Contents**

[TOC]

## Introduction

When creating a Python package or module, there may be a need to include non-Python files such as configuration files, templates, images, or data files. These files are typically required for the package or module to function properly or to provide optional features that depend on them.

Python provides several ways to include non-Python files in a package or module, but using `setup.py` is the most common and recommended method. In this article, we will explore how to include non-Python files with `setup.py` using examples and best practices.

## Including non-Python files with `setup.py`

To include non-Python files with `setup.py`, we use the `package_data` argument in the `setup()` function. The `package_data` argument takes a dictionary that specifies the package names and patterns of files to include. For example:

```python
from setuptools import setup, find_packages

setup(
    ...
    packages=find_packages(),
    package_data={
        'my_package': ['data/*.txt', 'templates/*.html'],
        'my_other_package': ['images/*.png'],
    },
    ...
)
```

In the example above, we are using `find_packages()` to discover all the packages in our project and include them in the distribution. We then use `package_data` to specify the files to include in each package. The patterns in `package_data` use a Unix-style file matching syntax and can include directories, file extensions, wildcards, etc.

All the files specified in `package_data` will be included in the distribution package when we run `python setup.py sdist` or `python setup.py bdist_wheel`. They will also be installed alongside the Python modules when the package is installed with `pip` or `easy_install`.

### Examples

Let's see some practical examples of including non-Python files with `setup.py`.

#### Example 1: Including a configuration file

Assume we have a package `my_package` that requires a configuration file `config.ini` in its root directory. We can include this file by adding the following line to `setup.py`:

```python
...
setup(
    ...
    package_data={
        'my_package': ['config.ini'],
    },
    ...
)
...
```

This will include `config.ini` in the distribution package and install it in the same directory as the Python modules.

#### Example 2: Including data files and templates

Assume we have a package `my_package` that provides a data file `data.csv` and a template file `report_template.html`, both located in the `my_package/data` directory. We can include both files by adding the following line to `setup.py`:

```python
...
setup(
    ...
    package_data={
        'my_package': ['data/*.csv', 'data/*.txt', 'templates/*.html'],
    },
    ...
)
...
```

This will include all `.csv` and `.txt` files in the `my_package/data` directory and all `.html` files in the `my_package/templates` directory.

### Best practices

When including non-Python files with `setup.py`, it is important to follow some best practices to ensure a smooth and reliable distribution and installation process:

- Use `find_packages()` to discover all the packages in the project and include them in the distribution.
- Specify the files to include in each package using the `package_data` argument in `setup()`.
- Use Unix-style file matching syntax in `package_data` to specify file patterns.
- Specify the encoding of text files explicitly, especially if they are in a non-ASCII encoding.
- Include only necessary files and avoid cluttering the distribution with irrelevant or temporary files.
- Include a `MANIFEST.in` file to specify additional files that are not included in `package_data`, such as readme files, license files, or scripts.
- Test the distribution package by installing it in a clean virtual environment and ensuring that all the files and features work as expected.

## Conclusion

Including non-Python files with `setup.py` is a common and essential task in Python package development. By using the `package_data` argument in `setup()`, we can include arbitrary files in the distribution package and ensure they are installed alongside the Python modules. Following the best practices outlined in this article will help to create reliable and maintainable packages that provide rich and versatile functionality.
