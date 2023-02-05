---
title: There is an import error on windows saying that there is no module named numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Install the numpy module using the command `pip install numpy` in the command line.
---

**Contents**

[TOC]

# Solution 1

## Installing Numpy

The easiest way to install numpy on Windows is to use the Python Package Index (PyPI). To do this, open the command prompt and type `pip install numpy`. This will install the latest version of numpy. 

## Alternative Ways to Install Numpy

If you don't want to use pip, you can also download the source code from the numpy website and install it manually. You can also install numpy using Anaconda, a popular Python distribution.

# Solution 2

## Installing Numpy

The easiest way to install numpy on Windows is to use the Python Package Index (PyPI). To do this, open the command prompt and type `pip install numpy`. This will install the latest version of numpy.

## Verifying Numpy Installation

Once numpy is installed, you can verify the installation by typing `python -c "import numpy; print(numpy.__version__)"` in the command prompt. This will print the version of numpy that is installed.

## Troubleshooting

If you are still getting the error after installing numpy, try updating pip and reinstalling numpy. If that doesn't work, try using a different version of Python.
