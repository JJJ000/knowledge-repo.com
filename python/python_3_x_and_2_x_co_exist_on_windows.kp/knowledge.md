---
title: Is it possible to have both Python 3.x and 2.x installed on a single windows computer?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, it is possible to install Python 3.x and 2.x on the same Windows computer by installing them in separate directories.
---

**Contents**

[TOC]

# Yes, you can install Python 3.x and 2.x on the same Windows computer

## Install Python 2.x and 3.x using official installers

The easiest way to install Python 2.x and 3.x on the same Windows computer is to download and install the official installers from the official website. You can download the latest version of Python 2.x from the Python 2 website and the latest version of Python 3.x from the Python 3 website. During the installation process, you can choose the folder where you want to install each version of Python.

## Use virtual environments

Another way to use Python 2.x and 3.x on the same Windows computer is to use virtual environments. Virtual environments allow you to create isolated Python environments where you can install different packages and versions of Python. You can create a virtual environment for Python 2.x and another one for Python 3.x and switch between them as needed.

You can use the virtualenv package to create virtual environments for Python. You can install virtualenv using pip, which is the package installer for Python. Open a command prompt window and enter the following command to install virtualenv:

```
pip install virtualenv
```

Once you have installed virtualenv, you can create a new virtual environment by entering the following command:

```
virtualenv my_env
```

Replace "my_env" with the name you want to give your new environment. You can create one virtual environment for Python 2.x and another one for Python 3.x.

## Use conda

Another option to run Python 2.x and 3.x together is to use conda. Conda allows you to create and manage environments for scientific computing and data science in Python. With conda, you can create different environments that have different versions of Python and install packages without conflicts.

To use conda, you need to install Miniconda, which is a smaller version of Anaconda, a Python distribution that includes many commonly used packages for scientific and data analysis. You can download and install Miniconda from this link: https://docs.conda.io/en/latest/miniconda.html. After installing Miniconda, you can create a new environment with Python 2.x with the following command:

```
conda create --name my_env python=2
```

Replace "my_env" with the name you want to give your new environment. You can create one environment for Python 2.x and another for Python 3.x. You can activate an environment using the following command:

```
conda activate my_env
```

When you are done using an environment, you can deactivate it using the following command:

```
conda deactivate
```
