---
title: Can you suggest a way to capture a numpy warning as an exception instead of only for testing purposes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can catch NumPy warnings as exceptions by using the `numpy.seterr` function with the appropriate `raise` parameter value.
---

**Contents**

[TOC]

## Introduction

NumPy is a popular Python library used for numerical computing, scientific computing, and data analysis. It is known for its powerful n-dimensional array object, which is used extensively in various scientific and data computing applications.

While using NumPy, it is common to encounter some warning messages, such as division by zero, invalid value encountered in the array, etc. These warning messages can disrupt program execution and lead to unexpected results if not handled properly.

In such cases, it is necessary to catch these warnings and handle them appropriately, as exceptions would be caught. In this guide, we will explore how to catch NumPy warning messages as exceptions and handle them properly.


## Catching NumPy Warnings as Exceptions

Catching NumPy warnings as exceptions can be done by using NumPy's Warning module. The first step is to import the Warning module and its subclasses into your Python script:

```python
import warnings
from numpy.lib import NumpyWarning
from numpy.core import VisibleDeprecationWarning
```

Once these modules are imported, you can catch NumPy warning messages as exceptions by calling the `warnings.filterwarnings()` function with the appropriate warnings module.

```python
warnings.filterwarnings('error', category=NumpyWarning)
warnings.filterwarnings('error', category=VisibleDeprecationWarning)
```

The `filterwarnings()` function takes a filter action and a warning category as its arguments. In this example, we are setting the filter action to `error`, which means that any warning message matching the specified category will be raised as an exception.

Note that you can catch specific types of NumPy warnings by using the appropriate subclass of the Warning module.

## Handling NumPy Warnings

Once you have caught NumPy warnings as exceptions, you can handle them just like regular exceptions. You can use try-except blocks to catch the exception and handle it appropriately.

```python
try:
    # Some NumPy code that raises a warning
except NumpyWarning:
    # Handle the warning appropriately
```

In this example, we are catching any NumPy warning messages raised within the try block and handling them in the except block. You can add more except blocks for other types of warnings if needed.

## Resetting NumPy's Warning Filters

After you are done handling NumPy warning messages, it is essential to reset NumPy's warning filters to their default settings. This ensures that any subsequent NumPy warnings are not caught as exceptions unintentionally.

```python
warnings.filterwarnings('default', category=NumpyWarning)
warnings.filterwarnings('default', category=VisibleDeprecationWarning)
```

By calling the `filterwarnings()` function with the `default` filter action, we can reset NumPy's warning filters to their default settings.

## Conclusion

Catching NumPy warning messages as exceptions and handling them properly is essential for the smooth execution of programs that use NumPy. By using NumPy's Warning module and try-except blocks, we can catch and handle NumPy warnings just like regular exceptions. Additionally, remember to reset NumPy's warning filters to their default settings to avoid unintentionally catching warnings in subsequent code.
