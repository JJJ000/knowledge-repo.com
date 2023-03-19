---
title: The Python error "module object does not have 'serial' attribute"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The module used does not have the attribute `Serial`.
---

**Contents**

[TOC]

# Introduction
The Python AttributeError occurs when an instance of a class has a non-existent attribute. In this case, the error message indicates that the module object being referred to does not have the Serial attribute.

# Check module installation
One possible cause of this error is not having the module required for serial communication installed. In this case, the pySerial module is needed to utilize the Serial attribute. You can check if this module is installed by running `pip list` in your command prompt or terminal. If it is not installed, you can install it using `pip install pyserial`.

# Check import statement
Another possible cause of this error is an incorrect import statement. Even if the pySerial module is installed, if the import statement refers to a different name or a different module, the Serial attribute will not be found. Make sure that the import statement is correct and refers to the pySerial module like this: `import serial`.

# Check syntax and code logic
If the first two possible causes have been ruled out, it is possible that there is an error in the syntax or code logic. Review the code and make sure that the instance of the Serial attribute is being called correctly and that it is compatible with the version of the pySerial module installed.

# Conclusion
In summary, the Python AttributeError error message indicating that a module object has no attribute 'Serial' can be caused by an incorrect module installation, an incorrect import statement, or an error in the syntax and code logic. By checking these possible causes, the error can be fixed and the correct functioning of the Serial attribute can be ensured.
