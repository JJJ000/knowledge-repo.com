---
title: How to import files in Python using a path relative to the current working directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To import from a relative path in Python, use a dot notation to indicate the path relative to the current module.
---

**Contents**

[TOC]

# Overview
Python provides several ways to import modules or files from different directories or paths. One such method is importing from a relative path. In this tutorial, we'll look at the steps involved in importing from a relative path in Python.

# Steps Involved
1. Determine the relative path: The first step is to determine the relative path of the file that needs to be imported. The relative path is the path of the file or module with respect to the directory where the importing file is present.

2. Create an empty __init__.py file: To create a package, you need to have an empty __init__.py file in the directory. This file is used to mark the directory as a Python package.

3. Import the module or file: Now that the relative path and __init__.py file are in place, you can import the module or file using the dot notation. For example, if the file to be imported is present one directory up from the current directory, you can use the following code: `from ..filename import function_name`.


# Example

Let's assume that we have the following directory structure.

```
project/
    main.py
    utils/
        __init__.py
        helper.py
```

helper.py contains the following function:
```
def greet(name):
    print(f"Hello, {name}!")
```

To import and use this function in main.py, we can use the following code:

```
from utils.helper import greet

greet("Alice")  # Output: Hello, Alice!
```

Here, we're importing the `greet` function from `helper.py` using the relative path `utils/helper.py`. Note that we've added an empty `__init__.py` file in the `utils` directory to mark it as a Python package.

We can also use dot notation to import `greet` function from a relative path:

```
from ..utils.helper import greet

greet("Alice")  # Output: Hello, Alice!
```

Here, we're importing the `greet` function using a relative path of `..utils/helper.py`. Note the use of two dots to indicate that the file is located one directory up from the current directory.
