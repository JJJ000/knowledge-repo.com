---
title: The module is not found by Python in the same directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Make sure the module`s name matches the filename and check if there is an \_\_init\_\_.py file in the folder.
---

**Contents**

[TOC]

# Introduction

Python is a high-level programming language that is widely used for various programming purposes. In Python, we can create and use our own modules to organize and simplify our code. However, sometimes, even if the module is placed in the same folder as the Python file, Python may not be able to find it. This article explains some possible reasons why Python can't find the module in the same folder and suggests solutions to fix the issue.


# Check the Module Name and File Extension

The first thing to check when Python can't find a module is the module name and file extension. Python requires that the module file name and the module name inside the file match. For example, if the module is named "example", then the file that contains the module should be named "example.py". If the file name and module name don't match, Python won't be able to find the module.

Another thing to check is the file extension. Python modules should have the ".py" file extension. If the module file has a different extension, Python won't be able to find it. Therefore, make sure that the module file has the correct name and extension.


# Check the PYTHONPATH Environment Variable

The PYTHONPATH environment variable is used by Python to find modules. If Python can't find a module in the same folder, it may be because the folder is not in the PYTHONPATH. To check the PYTHONPATH variable, open the terminal or command prompt and type:

```
echo $PYTHONPATH
```

If there is no output, it means that the PYTHONPATH variable is not set. To add the current folder to the PYTHONPATH, type:

```
export PYTHONPATH=$PYTHONPATH:.
```

This will add the current folder to the PYTHONPATH. Afterward, run the Python file and see if Python can find the module.


# Use Absolute Import

In Python, we can use absolute import to specify the exact location of the module. Absolute import allows us to import modules from any location by explicitly specifying the file path. To use absolute import, we need to add the folder containing the module to the sys.path list. Here is an example of how to use absolute import:

```python
import os
import sys
sys.path.append(os.path.abspath('./'))

import example
```

In this example, we add the current folder to the sys.path list and use absolute import to import the "example" module from the folder. This will ensure that Python can find the module even if it's not in the PYTHONPATH.

# Conclusion

When Python can't find a module in the same folder, there are several reasons and solutions to consider. By checking the module file name and extension, setting the PYTHONPATH variable, and using absolute import, we can usually solve the problem and make Python find the module.
