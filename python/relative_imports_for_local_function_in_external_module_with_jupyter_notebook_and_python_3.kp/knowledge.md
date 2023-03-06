---
title: Using Python 3 in jupyter notebook, it is possible to employ relative imports in order to import a local function from a module that is located in a different directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the dot notation to specify the relative path from the current directory to the target module and then import the function using the from keyword from ..module\_directory.target\_module import target\_function.
---

**Contents**

[TOC]

Section 1: Understanding relative and absolute imports

In Python, there are two types of imports: relative imports and absolute imports. 

Relative imports are used when importing modules within the same package or subpackage. These are specified with a "." before the module name, indicating that the module is located in the current package or subpackage.

Absolute imports are used when importing modules from a different package or subpackage. These are specified with the entire path of the module, starting from the root directory of the project.

In general, it is recommended to use absolute imports whenever possible, as they make the module dependencies more explicit and reduce the risk of naming conflicts.

Section 2: Importing local functions from a module in another directory

To import local functions from a module housed in another directory, we can use relative imports. Here's an example:

Consider a file named 'my_module.py' in a directory named 'my_directory', which contains a function 'my_function':

```
my_directory/
    my_module.py
```

```
# my_module.py

def my_function():
    print("Hello World!")
```

To import this function in a Jupyter Notebook, located in the parent directory, we can use a relative import as follows:

```
from my_directory.my_module import my_function
```

This imports the 'my_function' from 'my_module.py' located in the 'my_directory' directory.

Section 3: Caveats when using relative imports

When using relative imports, it is important to note the following:

1. The script that is importing the module needs to be located at a higher level of the directory hierarchy.
2. The directory containing the imported module needs to have an '__init__.py' file, indicating that it is a package.
3. The syntax for relative imports is different in Python 2 and 3. In Python 2, relative imports are specified using the "from .module import name" syntax, whereas in Python 3, the syntax is "from . import module".

Section 4: Conclusion

In this answer, we discussed the differences between relative and absolute imports and demonstrated how to import local functions from a module in another directory using relative imports in a Jupyter Notebook. We also discussed some important caveats to keep in mind when using relative imports in Python.
