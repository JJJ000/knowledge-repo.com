---
title: When the parent class does not inherit from object, super() encounters an error of typeerror "argument 1 must be type, not classobj"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python 3, classes must inherit from object in order for super() to work properly.
---

**Contents**

[TOC]

Section 1: Introduction
- Briefly introduce the concept of super() in Python.
- Mention the common usage of super() to call a method from a parent class.

Section 2: The Issue
- Explain the error message "argument 1 must be type, not classobj" that occurs when super() is used with a parent class that does not inherit from object.
- Discuss how this error occurs because objects in Python 2.x are not new-style classes by default, and super() requires new-style classes.

Section 3: Solution 1 - Inherit from object
- Provide the first solution to the issue: inherit from object. 
- Explain how this immediately fixes the issue, as inheriting from object automatically creates a new-style class.
- Provide an example of how to modify the parent class to inherit from object.

Section 4: Solution 2 - Use classic super()
- Provide a second solution: use classic super() instead of super().
- Explain how classic super() is able to work with old-style classes, but does not guarantee the same method resolution order (MRO) as super().
- Provide an example of how to modify the child class to use classic super(). 

Section 5: Conclusion
- Summarize the issue, and the two solutions to fix it.
- Mention that using new-style classes and super() is recommended, but sometimes classic super() may be necessary.
