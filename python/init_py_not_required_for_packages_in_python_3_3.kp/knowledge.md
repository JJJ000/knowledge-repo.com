---
title: Do packages in Python 3.3+ not require __init__.py?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, it is still required for packages in Python 3.3+.
---

**Contents**

[TOC]

# No
__init__.py is still required for packages in Python 3.3+ in order for Python to recognize the directory as a package.

# Why
Python 3.3+ allows for packages to be defined without an __init__.py file, but the __init__.py file is still necessary for the package to be recognized as a package. Without the __init__.py file, Python will not recognize the directory as a package, and therefore any modules or packages contained within the directory will not be available.

# Benefits
Having an __init__.py file allows developers to define special attributes and functions that will be available to all modules within the package. This allows for a more organized and efficient way to create and use packages.

# Conclusion
In conclusion, __init__.py is still required for packages in Python 3.3+. This is necessary for the package to be recognized as a package and for the modules and packages contained within the directory to be available.
