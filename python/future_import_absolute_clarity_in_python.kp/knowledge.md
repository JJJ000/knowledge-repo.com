---
title: Could you explain the functionality of 'from __future__ import absolute_import'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: It ensures that modules within a package are imported absolutely rather than relative to the importing module.
---

**Contents**

[TOC]

# Introduction 
The `from __future__ import absolute_import` is a statement in Python used to enable the use of absolute imports in a Python module. It is often used when working with modules that have the same name as a built-in module in Python.

# Background
In Python, when importing modules, there are two types of imports - relative imports and absolute imports. Relative imports work by specifying the path to the module relative to the current module, while absolute imports work by specifying the full path to the module.

# Enabling Absolute Import
To enable absolute imports in a Python module, the `from __future__ import absolute_import` statement is added at the top of the module. This statement allows the use of absolute imports by default, overriding any relative imports that may be present in the module.

# Advantages of Absolute Import
There are several advantages of using absolute imports in Python. Firstly, absolute imports make it easier to identify the exact location of a module, making it easier to debug and maintain modules. Secondly, absolute imports prevent naming conflicts between modules with similar names, especially when working with third-party modules. Finally, absolute imports make it easier to import modules from a different location, improving the modularity and portability of your code.
