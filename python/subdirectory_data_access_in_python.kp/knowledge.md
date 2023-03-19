---
title: Retrieve information from a subdirectory within a package
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use a period (.) in the import statement to access modules in subdirectories within a package in Python.
---

**Contents**

[TOC]

Section 1: Introduction 

Python is an interpreted, high-level, and general-purpose programming language. It was created in the late 1980s by Guido van Rossum and has been evolving ever since. One of the strengths of Python is its large ecosystem of packages that make it easy to perform a wide range of tasks.

When working with packages in Python, it is common to create subdirectories within the package directory. These subdirectories can contain data that the package needs to function correctly. In this article, we will discuss how to access data in package subdirectories in Python.

Section 2: Using the pkg_resources module

The pkg_resources module is part of the setuptools package, which is a collection of Python packages that extend the functionality of the standard library. The pkg_resources module provides an API for working with files and resources in packages.

To access data in a package subdirectory using the pkg_resources module, you can use the resource_filename() function. This function takes two arguments: the name of the package and the relative path to the file or directory you want to access.

Here is an example:

```python
from pkg_resources import resource_filename

file_path = resource_filename('mypackage', 'subdir/data.txt')
with open(file_path, 'r') as f:
    data = f.read()
```

In this example, we are accessing the data.txt file in the mypackage/subdir/ directory. The resource_filename() function returns the absolute path to the file, which we can then use to open and read the file.

Section 3: Using the pathlib module

The pathlib module is a newer module in Python that provides a more object-oriented way of working with paths. It was introduced in Python 3.4 and provides a concise syntax for working with file and directory paths.

To access data in a package subdirectory using the pathlib module, you can use the Path() function to create a Path object pointing to the package directory. You can then use the / operator to navigate to the subdirectory and file you want to access.

Here is an example:

```python
from pathlib import Path

package_dir = Path(__file__).resolve().parent
file_path = package_dir / 'subdir' / 'data.txt'

with open(file_path, 'r') as f:
    data = f.read()
```

In this example, we are first creating a Path object pointing to the package directory using the __file__ variable (which contains the path to the current file) and the resolve() and parent methods. We then use the / operator to navigate to the subdir/data.txt file and open it for reading.

Section 4: Conclusion

In this article, we have discussed how to access data in package subdirectories in Python. We have shown two different methods for doing so: using the pkg_resources module and using the pathlib module. Both methods have their advantages and can be used in different situations depending on your needs.
