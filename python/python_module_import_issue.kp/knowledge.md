---
title: I am unable to bring in my own modules in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Make sure the module file is in the same directory as your script or add the directory path to your system`s PYTHONPATH.
---

**Contents**

[TOC]

Section 1: Check the module file name and location

Make sure that the module file you are trying to import has the correct file name and is saved in the correct location. If the file name is incorrect or the file is saved in a different location, then Python will not be able to find and import the module.

Section 2: Check the PYTHONPATH environment variable

The PYTHONPATH environment variable contains a list of directories where Python looks for module files. If the module file is saved in a directory that is not included in the PYTHONPATH, Python will not be able to find and import the module. Check the value of PYTHONPATH to make sure it includes the directory where the module file is saved.

Section 3: Check the syntax of the import statement

Make sure that the syntax of your import statement is correct. The syntax for importing a module is:

```
import module_name
```

If you are importing a function or variable from a module, the syntax is:

```
from module_name import function_name
```

If you are importing a module with an alias, the syntax is:

```
import module_name as alias
```

Check that the module name and function/variable name are spelled correctly and that the import statement is in the correct format.

Section 4: Check for circular imports

Circular imports occur when two or more modules import each other. This can cause issues with importing and can result in import errors. Check for circular imports in your code and resolve any circular dependencies by reorganizing your code or using conditional imports.
