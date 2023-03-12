---
title: The degree to which global variables can be seen in modules that have been imported
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Global variables in one module are not visible in imported modules by default, unless specifically imported or made part of a shared namespace.
---

**Contents**

[TOC]

1. Introduction
Python language provides the ability to import modules to be used in a program. These modules contain various functions, classes, and variables that can be used directly in the program. When importing a module, all the variables defined in the module become available in the importing code. However, the visibility of these variables can be restricted based on the scope of the variables.

2. Global variables in imported modules
Global variables are variables that are defined at the top-level of a module and are accessible throughout the module. When a module is imported, all the variables defined in the module become global variables in the importing code. The global variables can be accessed using the module name followed by the variable name.

For example, if a module named `my_module` contains a global variable `x`, it can be accessed in the importing code as `my_module.x`. If the value of the variable is changed in the importing code, it will also affect the value of the variable in the original module.

3. Restricting visibility of global variables
Although global variables are accessible in the importing code, their visibility can be restricted by using proper encapsulation techniques. One of the techniques is to use the `__all__` attribute in the module. This attribute is a list of strings containing the names of the variables that should be visible in the importing code.

For example, if a module named `my_module` contains three variables `x`, `y`, and `z`, but only the variables `x` and `y` should be visible in the importing code, the `__all__` attribute can be set as follows:

```python
__all__ = ['x', 'y']
```

In this case, only the variables `x` and `y` can be accessed in the importing code using the module name as a prefix.

4. Conclusion
In summary, global variables in imported modules are accessible in the importing code. However, their visibility can be restricted by using proper encapsulation techniques. The `__all__` attribute in the module can be used to specify the names of the variables that should be visible in the importing code.
