---
title: What can I do to make numpy members recognizable by pylint?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Install the numpydoc plugin for Pylint.
---

**Contents**

[TOC]

Enabling Pylint to recognize NumPy members in Python

NumPy is a popular package for scientific computing in Python, but Pylint may not recognize its members by default. Here are some steps you can take to enable Pylint to recognize NumPy members:


1. Install Pylint and NumPy

Make sure you have Pylint and NumPy installed in your Python environment. You can do this by running the following commands in your terminal:

```
pip install pylint
pip install numpy
```

2. Configure Pylint

Create a `pylintrc` file in your project directory, if you don't already have one. This file allows you to configure Pylint's behavior for your project. Add the following lines to the file:

```
[MASTER]
extension-pkg-whitelist=numpy

[TYPECHECK]
ignored-modules=numpy
```

The `extension-pkg-whitelist` option tells Pylint to recognize NumPy as a valid package, while the `ignored-modules` option tells Pylint to ignore NumPy when it performs type checking.

3. Run Pylint with the `--extension-pkg-whitelist` option

When running Pylint, pass the `--extension-pkg-whitelist=numpy` option to tell Pylint to recognize NumPy. Here's an example command:

```
pylint --extension-pkg-whitelist=numpy my_module.py
```

This will run Pylint on `my_module.py` and enable NumPy member recognition.

4. Use the correct NumPy namespace

Finally, make sure you are using the correct NumPy namespace in your code. NumPy has a number of submodules, such as `numpy.random` for random number generation and `numpy.linalg` for linear algebra operations. Make sure you import and use the correct submodule for your needs.

By following these steps, you should be able to enable Pylint to recognize NumPy members in your Python code.
