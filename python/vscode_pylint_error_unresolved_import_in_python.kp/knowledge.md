---
title: How to resolve 'unresolved import' error in visual studio code with pylint?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The `unresolved import` error in Visual Studio Code can be resolved by adding the root directory of the project to the `python.path` setting in the workspace or user settings.
---

**Contents**

[TOC]

Section 1: Overview
If you're a Visual Studio Code user working with Python, you may encounter an unresolved import error from the Pylint linter. This error indicates that Pylint can't find the module you're trying to import, so it can't analyze the code inside that module. Solving this error is important because it impacts the quality of your code and, in some cases, can lead to unexpected or hard-to-debug errors.

Section 2: Possible Causes
There are several reasons why Pylint may encounter an unresolved import error. Some of the most common causes are:
- The module you're trying to import isn't installed or isn't installed correctly.
- The module isn't in the same directory as your Python file, and Python isn't able to find it.
- You need to add the module to your PYTHONPATH environment variable.
- There's a circular import dependency in your code, which means you're trying to import a module that's dependent on the module you're currently working on.

Section 3: Solutions
To solve the unresolved import error, here are some possible solutions:
- Make sure the module you're trying to import is installed correctly. You can use your package manager (e.g. pip) to check the installation status of the module.
- Move the module to the same directory as your Python file, or add the directory where the module is located to your PYTHONPATH environment variable.
- If you're using a virtual environment, make sure the virtual environment is activated before you run your Python script.
- Check for circular import dependencies in your code and resolve them. This may require changing the structure of your code or importing modules at a different point in the execution flow.

Section 4: Conclusion
By understanding the causes of the unresolved import error in Pylint, you can take the necessary steps to solve this error and ensure that your Python code is of high quality. With the right configuration and troubleshooting, you can use Pylint to catch errors early in the development process, leading to more efficient coding and fewer bugs in your final product.
