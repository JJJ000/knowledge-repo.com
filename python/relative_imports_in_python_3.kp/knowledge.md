---
title: Importing modules in Python 3 relative to the current module's location
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Relative imports allow modules within the same directory to reference each other using syntax such as `from . import module`.
---

**Contents**

[TOC]

# Syntax
The syntax for relative imports in Python 3 is `from .[module] import [name]`.

# Example
For example, if you have two modules in the same directory, `module1.py` and `module2.py`, and you want to import the `foo` function from `module1.py` into `module2.py`, you can use the following syntax:

```
from .module1 import foo
```

# Benefits
Relative imports allow you to keep your code organized and prevent you from having to type out the full path to the module you want to import. This makes it easier to maintain and update your code.

# Limitations
Relative imports can only be used within the same directory. If you need to import a module from a different directory, you will need to use an absolute import.
