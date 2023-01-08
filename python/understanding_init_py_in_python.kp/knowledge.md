---
title: What is the purpose of __init__.py?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: __init__.py is a special Python file used to indicate that a directory is a Python package.
---

**Contents**

[TOC]

### Purpose
The `__init__`.py file is used to indicate that the directory it is contained in is a Python package directory.

### Content
The `__init__`.py file can contain code that will be executed when the package is imported. It can also be used to initialize variables or set default values.

### Structure
The `__init__`.py file is usually empty, but it can contain code that will be executed when the package is imported.

### Example
For example, the following `__init__`.py file would set the default value of the variable ‘foo’ to ‘bar’ when the package is imported:
```python
foo = 'bar'
```