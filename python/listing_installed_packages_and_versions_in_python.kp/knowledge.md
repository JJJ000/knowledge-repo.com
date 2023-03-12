---
title: What is the method to display a list of all the packages installed along with their versions using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can list all installed packages and their versions in Python using the command `pip freeze` in the command prompt or terminal.
---

**Contents**

[TOC]

Section 1 - Introduction:

In this tutorial, we will learn how to list all installed packages and their versions in Python. We will use the built-in pip module, which is the standard package manager for Python.

Section 2 - Method 1: Using `pip freeze` command

The easiest way to list all installed packages and their versions is to use the `pip freeze` command in the terminal. This command will return a list of all installed packages with their versions. To execute the `pip freeze` command from Python code, we can use the `subprocess` module.

```python
import subprocess

# Execute pip command, get list of installed packages
reqs = subprocess.check_output(['pip', 'freeze'])
print(reqs)
```

Section 3 - Method 2: Using `pkg_resources` module

Another way to list all installed packages and their versions is to use the `pkg_resources` module. This method has the advantage of being more Pythonic and not requiring the use of an external command. The `pkg_resources` module is included in the standard library and provides an API for working with packages and their resources.

```python
import pkg_resources

# Get list of installed packages
installed_packages = pkg_resources.working_set

# Print package name and version
for package in installed_packages:
    print("{}=={}".format(package.key, package.version))
```

Section 4 - Conclusion:

We have learned two ways to list all installed packages and their versions in Python. The first method uses the `pip freeze` command and subprocess module, while the second method uses the `pkg_resources` module. Depending on the use case, one method may be more suitable than the other.
