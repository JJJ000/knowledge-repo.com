---
title: Is it necessary to have blas for Python scipy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, Python SciPy needs BLAS for optimized linear algebra operations.
---

**Contents**

[TOC]

Introduction:
-------------
BLAS stands for Basic Linear Algebra Subprograms. It is a library of routines which provide a number of standard building blocks for performing basic vector and matrix operations. SciPy is a python-based library that is used for scientific calculation and numerical computation.

Python SciPy Library:
----------------------
Python SciPy library has a number of modules including `scipy.linalg` which provides an interface to BLAS routines. The scipy.linalg module uses fast BLAS routines to provide optimized linear algebra operations. 

Need for BLAS in SciPy:
------------------------
BLAS is not necessary for using SciPy, but it can significantly improve the performance of the library. BLAS provides optimized routines for common linear algebra operations, and using these optimized routines can greatly improve the speed of calculations. Using BLAS also allows for efficient parallelization of operations, which is particularly important for large datasets.

Alternatives to BLAS:
----------------------
While BLAS can greatly improve the performance of SciPy, there are alternatives available. The OpenBLAS library provides an open-source implementation of BLAS routines, and is a popular choice for many scientific computing applications. Additionally, other math libraries such as Intel MKL and ATLAS provide optimized routines for linear algebra operations, that can also be used without BLAS. 

Conclusion:
------------
While not strictly necessary, using BLAS in conjunction with SciPy can greatly improve the performance of scientific computing applications. Other libraries such as OpenBLAS, ATLAS, and MKL provide alternatives to using the BLAS library directly.
