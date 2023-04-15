---
title: What is the process for bringing in other Python files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the `import` statement to import other Python files.
---

**Contents**

[TOC]

# Section 1: Importing Python Modules

The most common way to import a Python module is with the `import` statement. This statement allows you to access the functions and variables defined in the module. For example, to import the `math` module, you would type:

```python
import math
```

# Section 2: Importing Specific Functions

You can also import specific functions from a module. This is useful if you only need to use a few functions from a module, and don't want to import the entire module. To do this, use the `from` keyword followed by the module name, and then specify which functions you want to import. For example, to import the `sqrt` and `cos` functions from the `math` module, you would type:

```python
from math import sqrt, cos
```

# Section 3: Importing as Aliases

You can also import modules and functions using aliases. This is useful if you want to use a shorter name for a module or function. For example, to import the `math` module as the alias `m`, you would type:

```python
import math as m
```

# Section 4: Importing from Other Files

You can also import modules and functions from other Python files. To do this, you must first save the other file in the same directory as your current file. Then, use the `import` statement with the filename (without the `.py` extension). For example, to import the `my_module` module from the `my_file.py` file, you would type:

```python
import my_file
```
