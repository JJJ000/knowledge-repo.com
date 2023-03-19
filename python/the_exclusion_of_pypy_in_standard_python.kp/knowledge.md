---
title: What was the reason for pypy not being included in the standard Python installation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: PyPy was not included in standard Python because it is a separate implementation of the language with different goals and objectives.
---

**Contents**

[TOC]

Section 1: Introduction to PyPy
PyPy is an alternative implementation of the Python programming language. It is designed to be faster and more efficient than the standard CPython implementation, which is the reference implementation of Python. PyPy is written in Python and uses a Just-In-Time (JIT) compiler to improve performance.

Section 2: Differences between PyPy and CPython
Although PyPy and CPython are both implementations of the Python programming language, there are significant differences between the two. One of the main differences is that PyPy uses a JIT compiler, which can significantly improve performance in certain situations. Additionally, PyPy has a smaller memory footprint than CPython and can handle large amounts of data more efficiently.

Section 3: Reasons why PyPy was not included in standard Python
Despite the benefits of PyPy, there are several reasons why it was not included in standard Python. One reason is that PyPy is not fully compatible with all Python libraries and frameworks. This means that some code written for CPython may not work properly in PyPy, which could be a significant barrier to adoption.

Another reason is that PyPy has its own set of bugs and limitations that could make it unstable for certain use cases. Additionally, PyPy is a relatively new project and has not yet gained widespread adoption among Python developers.

Section 4: Conclusion
In conclusion, PyPy is a promising alternative implementation of the Python programming language that has several significant advantages over CPython. However, due to compatibility issues and other factors, it has not yet been included in standard Python. Nevertheless, PyPy remains a popular choice for developers looking to improve performance or reduce memory usage in their Python applications.
