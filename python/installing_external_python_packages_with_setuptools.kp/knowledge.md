---
title: What is the procedure to instruct setuptools to install a package that is not available on pypi?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `dependency\_links` parameter in your `setup.py` file to specify the URL of the package to be installed.
---

**Contents**

[TOC]

## Section 1: Introduction

Setuptools is a package installation tool in Python that installs packages from multiple repositories. If you have a package that is not on PyPI but you want to install it with setuptools, you can follow three possible approaches: 

1. Install the package from a local path using setuptools. 
2. Package the package into a distribution that setuptools can install.
3. Install the package manually and add it to the Python path.

In this article, we'll discuss each of these approaches in detail.

## Section 2: Installing a package from a local path

If you have the source code for a package that is not on PyPI, you can package it into a wheel or tar file, and use setuptools to install it from a local path. To do this, follow the steps below:

1. Create a source distribution (tar or zip file) of your package. You can create a source distribution using the `sdist` command from setuptools. 
```
python setup.py sdist
```

2. Create a wheel file for your package using the `bdist_wheel` command from setuptools. 
```
python setup.py bdist_wheel
```

3. Move the generated source distribution and wheel file to a directory on your machine.

4. Install the package using pip, specifying the local path to the wheel file.
```
pip install /path/to/wheel/file.whl
```

Setuptools will then install the package from the local path.

## Section 3: Creating a distribution that can be installed by setuptools

If you want to package a Python package into a distribution that can be installed by setuptools, follow these steps:

1. Create a source distribution (tar or zip file) of your package, as outlined in section 2.

2. Create a setup.py file for your distribution (if you don't already have one).

3. Use the `setuptools.setup` function to define your distribution. 

4. Upload your distribution to a repository that setuptools can access, such as PyPI or a private repository.

Once your package is uploaded to PyPI, you can install it using pip or easy_install, as shown below:
```
pip install mypackage
```

Setuptools will automatically download and install the package from PyPI.

## Section 4: Manually adding the package to the Python path

If you don't want to package your package into a distribution or install it from a local path, you can manually add the package to the Python path. To do this, follow these steps:

1. Download the package's source code.tar file from the source repository.

2. Extract the tar file to a directory on your local machine.

3. Add the directory containing the package to the PYTHONPATH environment variable, as shown below:
```
export PYTHONPATH=${PYTHONPATH}:/path/to/package
```

Setuptools will then be able to find the package and import its contents into your Python code.

## Conclusion

In this article, we've outlined three possible approaches for installing a Python package that is not on PyPI using setuptools. By following these approaches, you can install packages from repositories other than PyPI, or create your own distribution for your custom package.
