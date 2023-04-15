---
title: The error message "numpy/arrayobject.h no such file or directory" in cython is fatal
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You need to install the NumPy development headers to resolve this error.
---

**Contents**

[TOC]

Section 1: Overview
One of the main advantages of using Cython in Python is to improve the efficiency and speed of code execution. However, when working with Cython, you might come across a common error message: "fatal error: numpy/arrayobject.h: No such file or directory". This error can prevent you from running your code, and it is vital to understand how to resolve it.

Section 2: Understanding the Error Message
The error message "fatal error: numpy/arrayobject.h: No such file or directory" indicates that Cython is unable to find the header file for the NumPy array object. This error is usually caused by one of two reasons:

1. The NumPy module is not installed, or
2. The path to the NumPy header file is incorrect.

If you have verified that NumPy is installed and you still see this error message, the problem is most likely with the path to the header file.

Section 3: Resolving the Error
To resolve the "fatal error: numpy/arrayobject.h: No such file or directory" error, you need to ensure that Cython can find the NumPy header file. One way to do this is by adding the NumPy header file path to the include_dirs parameter in your Cython setup file.

Here is an example of how to modify the setup file:

```
from distutils.core import setup
from Cython.Build import cythonize
import numpy

setup(
    ext_modules=cythonize("your_code.pyx"),
    include_dirs=[numpy.get_include()]
)
```

This modification adds the NumPy header file path to the list of directories in the include_dirs parameter, allowing Cython to locate the header file.

Section 4: Conclusion
The "fatal error: numpy/arrayobject.h: No such file or directory" error message in Cython is usually caused by a missing or incorrect path to the NumPy header file. By adding the NumPy header file path to your Cython setup file, you can resolve this error and run your code successfully.
