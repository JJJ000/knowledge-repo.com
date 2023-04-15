---
title: Use pip to install a module for a particular version of python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To install a module using pip for a specific Python version, run the following command 
<code>pip3.7 install [module-name]</code> where 3.7 is the specific Python version.
---

**Contents**

[TOC]

Section 1: Introduction 
Pip is a package manager for Python that allows you to install and manage software packages written in Python. It comes pre-installed with Python versions 3.4 and above. However, if you have multiple versions of Python installed on your system, it is possible that pip is not associated with the correct version of Python. This can cause issues when trying to install packages. 

In this guide, we will discuss how to install a module using pip for a specific version of Python. 

Section 2: Checking for pip and Python version 
Before proceeding with installing the module, it is important to ensure that pip and the correct version of Python are installed on your system. You can check the version of Python by running the following command in your terminal: 

```python --version``` 

You can also check for the presence of pip by running:

```pip --version``` 

If pip is not installed, you can install it using the `get-pip.py` script. You can download the script from https://bootstrap.pypa.io/get-pip.py and run the following command:

```python get-pip.py``` 

Section 3: Installing a module for a specific Python version 
To install a module using pip for a specific version of Python, you will need to specify the correct version of pip and Python in your command. 

For example, if you have Python 3.7 installed and want to install the `numpy` package, the command would be: 

```python3.7 -m pip install numpy``` 

The `-m` argument ensures that the correct version of pip associated with Python 3.7 is used. 

Section 4: Conclusion 
In this guide, we have discussed how to install a module using pip for a specific version of Python. By specifying the correct version of pip and Python in your command, you can ensure that the package is installed correctly and associated with the correct version of Python.
