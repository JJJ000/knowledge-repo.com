---
title: Can you provide me a method for developing a namespace bundle in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To create a namespace package in Python, you need to create a directory with an \_\_init\_\_.py file, and add subsequent directories with their own \_\_init\_\_.py files that declare \_\_path\_\_ variables pointing to the parent directory.
---

**Contents**

[TOC]

## Section 1: Introduction

A namespace package is a way to split a single package across multiple directories, without the need for the directories to be directly connected or contained within each other. Namespace packages were added starting with Python's 3.3 release.

## Section 2: Creating a Namespace Package

Creating a namespace package in Python is a fairly straightforward process. Here are the steps:

1. Create a directory for your namespace package. The name of this directory should end with `-ns`.
```
mkdir my_namespace-ns
```
2. Inside this directory, create a `pkgutil.py` file. This will act as the package's initialization file.
```
touch my_namespace-ns/pkgutil.py
```
3. Open the `pkgutil.py` file and add the following Python code:
```
# my_namespace/pkgutil.py
__path__ = __import__('pkgutil').extend_path(__path__, __name__)
```
4. Create any packages or modules you want under the `my_namespace-ns` directory.

## Section 3: Using the Namespace Package

Now that you have created your namespace package, you can use it in your Python code like any other package. You can import the packages or modules you created in step 4 of Section 2 using the following syntax:
```
import my_namespace.a_module
from my_namespace import a_package
```

## Section 4: Packaging and Distributing Your Namespace Package

If you want to package and distribute your namespace package, you can create a `setup.py` file and include it in your project. Here is an example `setup.py` file for a namespace package:

```python
from setuptools import setup, find_namespace_packages

setup(
    name='my_namespace',
    version='0.1',
    packages=find_namespace_packages(include=['my_namespace.*']),
    install_requires=[
        # list any dependencies here
    ],
    # add any other configuration options you want
)
```

The key options to note in this `setup.py` file are:
- `packages=find_namespace_packages(include=['my_namespace.*'])` tells setuptools to include all sub-packages and modules under the `my_namespace` namespace package.
- `install_requires` is a list of any dependencies your package requires to run.

Once you have created your `setup.py` file, you can use `setuptools` to package and distribute your namespace package like any other Python package.
