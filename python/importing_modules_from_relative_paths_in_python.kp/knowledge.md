---
title: Load a module from a relative location
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can import a module from a relative path in Python using the `import` statement.
---

**Contents**

[TOC]

# Section 1: Importing a Module

In Python, modules can be imported from relative paths using the `import` statement.

# Section 2: Relative Path

A relative path is a path that is relative to the current working directory. This means that the path is not absolute, and instead will depend on the current working directory.

# Section 3: Syntax

The syntax for importing a module from a relative path is as follows:

```
import module_name from relative_path
```

# Section 4: Example

For example, if the module is located in the same directory as the current working directory, the following statement can be used:

```
import my_module from .
```
