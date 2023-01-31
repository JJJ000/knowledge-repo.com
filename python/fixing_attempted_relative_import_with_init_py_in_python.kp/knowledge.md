---
title: What steps are necessary to resolve the "attempted relative import in non-package" error even when an __init__.py file is present?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Add the absolute path of the module to the sys.path list.
---

**Contents**

[TOC]

# Section 1: Understanding the Error
The "Attempted relative import in non-package" error occurs when a user attempts to use a relative import in a file that is not part of a package. A package is a directory that contains an __init__.py file, which identifies the directory as a package and marks it for Python to include in its search path. A relative import is a method of importing a module or package that is relative to the current location of the importing file. 

# Section 2: Using an Absolute Import
The most straightforward way to fix the "Attempted relative import in non-package" error is to use an absolute import instead of a relative import. An absolute import is a method of importing a module or package that is based on its absolute path. To use an absolute import, the user must specify the full path to the module or package they are attempting to import. 

# Section 3: Creating a Package
Another way to fix the "Attempted relative import in non-package" error is to create a package. To create a package, the user must create a directory and add an __init__.py file to it. The __init__.py file is used to identify the directory as a package, and it also marks the directory for Python to include in its search path. Once the package is created, the user can use a relative import to import the module or package they are attempting to use. 

# Section 4: Adding to the Search Path
The user can also fix the "Attempted relative import in non-package" error by adding the directory containing the module or package they are attempting to import to the Python search path. To do this, the user must add the directory to the sys.path list. Once the directory is added to the list, Python will be able to find the module or package and the user will be able to use a relative import to import the module or package.
