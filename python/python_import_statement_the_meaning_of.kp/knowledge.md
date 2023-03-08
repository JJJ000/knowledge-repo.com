---
title: What is the meaning of a dot in a Python import statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The . in an import statement in Python refers to the current package or directory.
---

**Contents**

[TOC]

# Introduction

Python programmers can use the `import` statement to bring in code from other Python modules, either those in the standard library or those created by other developers. 

# The dot in an import statement

A dot in an import statement is used to import a submodule or object from a package/module. 

For example, consider the `math` module, which has a submodule called `trig`. To use the `trig` submodule, you can import it using the dot notation:

```python
import math.trig
```

# Importance of the dot in an import statement

Using the dot notation makes it easier to organize large codebases with many modules and submodules. It also allows you to selectively import specific objects or submodules from a larger module or package, rather than importing everything at once.

For example, if you only need the `pi` constant from the `math` module, you can import just that object using the dot notation:

```python
from math import pi
```

Using dot notation in import statements can also prevent naming conflicts, by allowing you to use the module or submodule name as a namespace.

# Conclusion

In summary, the dot in an import statement is used to import a submodule or object from a package/module. It is a useful tool for organizing large codebases and selectively importing specific objects or submodules.
