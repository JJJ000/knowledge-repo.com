---
title: There is an importerror indicating that the module named sklearn.cross_validation cannot be found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The module sklearn.cross\_validation has been renamed to sklearn.model\_selection in more recent versions of scikit-learn, so you should use `from sklearn.model\_selection import train\_test\_split` instead.
---

**Contents**

[TOC]

Section 1: Introduction
If you get an ImportError: No module named sklearn.cross_validation error in Python, it generally means that the cross_validation module is not installed for the scikit-learn library. The scikit-learn library provides tools for machine learning in Python, and the cross_validation module is a sub-module within it that provides tools for validating and testing models.

Section 2: Solution
The solution is to install scikit-learn and its dependencies, which can be done using pip, the package installer for Python. To install scikit-learn, open a terminal or command prompt, and type the following command:

`pip install -U scikit-learn`

This will install the latest version of scikit-learn and its dependencies. Once the installation is complete, you should be able to import the cross_validation module without any issues.

Section 3: Alternative solution
Sometimes, even after installing scikit-learn, you may still get the ImportError: No module named sklearn.cross_validation error. This may be due to a version mismatch between scikit-learn and your Python environment. In this case, you can try installing an older version of scikit-learn that is compatible with your version of Python. For example, if you are using Python 2.7, you can try installing scikit-learn version 0.20, which is compatible with Python 2.7. To install this version, type the following command:

`pip install -U scikit-learn==0.20`

Section 4: Conclusion
The ImportError: No module named sklearn.cross_validation error in Python can be easily resolved by installing scikit-learn and its dependencies using pip. If you still encounter the error, you may need to install an older version of scikit-learn that is compatible with your Python environment. With the scikit-learn library and its cross_validation module installed, you can leverage the tools and functions it provides for machine learning tasks in Python.
