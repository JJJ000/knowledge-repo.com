---
title: What is the process of installing Python packages in google's colab?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Python packages can be installed in Google`s Colab by using the !pip command followed by the package name.
---

**Contents**

[TOC]

# Overview
Python packages are collections of modules and libraries that extend the functionality of the Python programming language. Google's Colaboratory, commonly known as Colab, provides an interactive environment to write and execute Python code. Colab comes pre-installed with a set of commonly used packages. However, if additional packages are required, they can be installed using pip, the package management system for Python.

In this tutorial, we will go through the process of installing Python packages in Google's Colab.

# Steps
There are two ways to install packages in Colab:

1. Using pip
2. Using apt-get

## Using pip
Pip is a package management system that enables you to install and manage Python packages. To install a package using pip, you can use the following command:

```python
!pip install package_name
```

Here, `package_name` is the name of the package that you want to install. Note that the `!` symbol is used to execute shell commands from within the Colab notebook.

For example, to install the popular data manipulation library `pandas`, you can use the following command:

```python
!pip install pandas
```

To verify that the package has been successfully installed, you can run an import statement:

```python
import pandas as pd
```

If no errors are thrown, the package is successfully installed and ready to use.

## Using apt-get
Colab is based on a customized Ubuntu environment, and therefore, you can install packages available in the Ubuntu package repository using `apt-get`. To install a package using apt-get, you can use the following command:

```python
!apt-get install package_name
```

Here, `package_name` is the name of the package that you want to install. Note that the `!` symbol is used to execute shell commands from within the Colab notebook.

For example, to install the LaTeX Typesetting System, you can use the following command:

```python
!apt-get install texlive-full
```

Once the installation is complete, you can verify that the package has been installed by running the specific program associated with the package:

```python
!latex --version
```

If no errors are thrown, the package is successfully installed and ready to use.

# Conclusion
In this tutorial, we learned how to install Python packages in Google's Colaboratory. We covered two methods: using pip and using apt-get. By following these simple steps, you can easily install any Python package required for your project in Colab.
