---
title: The following error occurred scipy's wheels cannot be built using pep 517 and cannot be directly installed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: This error occurs when PEP 517 is used to build wheels for SciPy and it cannot be installed directly in Python.
---

**Contents**

[TOC]

Section 1: Introduction

In this error message, we see that it is related to the Scipy package, and specifically that it cannot build wheels using PEP 517, which means that it cannot be installed directly in Python. In this section, we will take a closer look at what this error means and how it can be resolved.

Section 2: Understanding PEP 517

PEP 517 is a Python Enhancement Proposal that defines a standard interface for build backends to produce packages from source code. This means that packages that adhere to this proposal can be built and installed more easily and consistently across different platforms and environments.

In practical terms, this means that if a package uses PEP 517, you can install it directly from source code without needing to manually build and compile it first. However, if a package does not use PEP 517, you may encounter errors like the one we are seeing with Scipy.

Section 3: Resolving the Error

There are a few different ways to resolve this error, depending on the specific situation you are encountering. Here are some potential solutions:

1. Upgrade pip: You can try upgrading pip to the latest version to ensure that you have the most up-to-date tools for installing packages. To do this, run "pip install --upgrade pip" in your command prompt or terminal.

2. Install from a pre-built binary: If you are encountering this error while trying to install Scipy, you can try downloading a pre-built binary from the Scipy website and installing it manually.

3. Use a different installation method: Depending on your system and environment, you may need to use a different method for installing Scipy or other packages that do not use PEP 517. For example, you may need to use a package manager like Conda or Anaconda instead of pip.

Section 4: Conclusion

In conclusion, the "Could not build wheels for scipy which use PEP 517 and cannot be installed directly in Python" error message indicates that the package cannot be installed directly due to its non-compliance with PEP 517. By upgrading pip, using a pre-built binary, or using a different installation method like Conda or Anaconda, you may be able to resolve this issue and successfully install the package.
