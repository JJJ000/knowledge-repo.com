---
title: What is the reason for attributeerror in Python 3.6.1 that states 'module 'enum' has no attribute 'intflag''?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The IntFlag class was added to the enum module in Python 3.6.2, so it is not available in Python 3.6.1.
---

**Contents**

[TOC]

Section 1: Introduction
Python 3.6.1 throws AttributeError: module 'enum' has no attribute 'IntFlag' when trying to use the IntFlag class from the enum module. This error occurs when using Python 3.6.1 or earlier versions because the IntFlag class was introduced in Python 3.6.2. In this answer, we will discuss why this error occurs and how to resolve it.

Section 2: The reason why the error occurs
The reason why Python 3.6.1 throws AttributeError: module 'enum' has no attribute 'IntFlag' is that the IntFlag class was introduced in Python 3.6.2. Therefore, if you are using Python 3.6.1 or earlier versions, the IntFlag class will not be available in the enum module, and hence you will get this error.

Section 3: How to resolve the error
There are two ways to resolve the AttributeError: module 'enum' has no attribute 'IntFlag' error. 

The first way is to upgrade to Python 3.6.2 or a later version. In Python 3.6.2 or later, the IntFlag class is available in the enum module, so you will not get the AttributeError: module 'enum' has no attribute 'IntFlag' error.

The second way is to define your own IntFlag class. You can define your own IntFlag class by inheriting from the IntEnum class and using bitwise operators (|, &, ^, ~) to combine the flag values. Here is an example of how to define your own IntFlag class:

```python
from enum import IntEnum
class IntFlag(IntEnum):
    FLAG_ONE = 1
    FLAG_TWO = 2
    FLAG_THREE = 4
```

With this, you can create and use an IntFlag enum in the same way as the built-in IntFlag class.

Section 4: Conclusion
Python 3.6.1 throws AttributeError: module 'enum' has no attribute 'IntFlag' because the IntFlag class was introduced in Python 3.6.2. This error can be resolved by upgrading to Python 3.6.2 or a later version or defining your own IntFlag class using bitwise operators like |, &, ^, and ~.
