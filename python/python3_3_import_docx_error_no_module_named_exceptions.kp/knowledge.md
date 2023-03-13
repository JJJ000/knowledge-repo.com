---
title: I encounter an importerror no module named 'exceptions' when attempting to import docx in python3.3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The `exceptions` module was removed in Python 3, so the error occurs when a module that relies on it is imported.
---

**Contents**

[TOC]

Section 1: Introduction
The error "ImportError: No module named 'exceptions'" can occur when importing a module in Python3.3, specifically when trying to import a module that is not compatible with Python3.

Section 2: Possible Cause
The most likely cause of this error is that the module you are trying to import was designed for Python2.x and is not compatible with Python3.x. In Python2.x, the exceptions module was a built-in module that included base classes for all exceptions. However, in Python3.x, the exceptions module was replaced by the built-in module "builtins".

Section 3: Solution
To solve this error, you need to ensure that you are using a version of the module that is compatible with Python3.x. If the module you are trying to use does not have a Python3 version, you can try using a compatibility library such as "six" which provides a compatibility layer between Python2 and Python3.

Section 4: Conclusion
In summary, the "ImportError: No module named 'exceptions'" error can occur when trying to import a module that is not compatible with Python3.x. To solve this error, you need to ensure that you are using a version of the module that is compatible with Python3.x or use a compatibility library such as "six".
