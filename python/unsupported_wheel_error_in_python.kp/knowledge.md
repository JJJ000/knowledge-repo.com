---
title: The file "filename.whl" is not compatible with this platform
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: This error occurs when attempting to install a wheel file that is not compatible with the current platform.
---

**Contents**

[TOC]

# Explanation

This error occurs when a Python wheel file is not compatible with the current platform. A wheel is a Python package format that contains all the files needed to run the package. Wheels are platform-specific, meaning they are only compatible with certain operating systems and versions of Python.

# Causes

The most common cause of this error is attempting to install a wheel that was created for a different operating system or version of Python than the one you are currently using. For example, if you are using Python 3.7 on a Windows computer, and you try to install a wheel that was created for Python 3.6 on a Mac, you will get this error.

Another cause of this error is attempting to install a wheel that is not compatible with the current version of Python. For example, if you are using Python 3.7 and you try to install a wheel that was created for Python 2.7, you will get this error.

# Solutions

The best solution is to make sure you are downloading the correct wheel for your platform and version of Python. You can find the correct wheel for your platform and version of Python on the Python Package Index (PyPI) website.

If you are unable to find the correct wheel for your platform and version of Python, you may need to create a wheel yourself. You can do this using the pip wheel command. For more information, see the pip wheel documentation.

Finally, if you are unable to find or create the correct wheel for your platform and version of Python, you may need to install the package from source.
