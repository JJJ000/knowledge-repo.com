---
title: When attempting to execute a Python script, an error message appears as "importerror no module named..."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The module you`re trying to import is not installed or not in the correct directory.
---

**Contents**

[TOC]

Section 1: Introduction

Python is widely used for scripting and automation. Occasionally, you may encounter an "ImportError: No module named" error when you try to run a Python script. This error occurs when the script cannot find the required module that it needs to execute. In this guide, we will discuss some common causes of this error and how to solve them. 

Section 2: Check the module name

The first thing to check is the module name. Verify that you have spelled it correctly and that it exists. You can use the Python Package Index (PyPI) or documentation to search for the module or package name. Make sure that you are using the correct name or alias when importing the module. 

Section 3: Check installation

Another common cause of "ImportError: No module named" is that the module is not installed. You need to make sure that the module is installed and accessible to your Python environment. You can verify the installation of the module using pip, which is the standard package management system for Python. You can use the following command to install a missing module:

`pip install <module-name>`

If you have multiple Python versions installed, make sure that you are installing the module for the correct version of Python. Alternatively, you can use virtual environments to isolate different environments and install packages without affecting the system-wide installation. 

Section 4: Check environment variables

Sometimes, Python may not be able to find the module because the module's path is not included in the `PYTHONPATH` environment variable. You can check if this is the case by running the following code:

```
import sys
print(sys.path)
```

This will print a list of paths that Python searches for modules. If you do not see the path to the module's location, you can add it to the `PYTHONPATH` environment variable. On Linux or macOS, you can export the environment variable by running the following command:

`export PYTHONPATH=$PYTHONPATH:/path/to/module`

On Windows, you can set the environment variable through the Control Panel or PowerShell. 

Section 5: Conclusion

"ImportError: No module named" is a common error that can occur when running a Python script. You can address this error by checking the module name, verifying installation, and setting up the correct environment variables. By following these steps, you should be able to resolve this error and run your Python scripts smoothly.
