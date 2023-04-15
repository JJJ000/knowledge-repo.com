---
title: What are the steps to avoid deprecation warnings in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can ignore deprecation warnings in Python by setting the warning filter to `ignore.`
---

**Contents**

[TOC]

## Introduction

Deprecation warnings occur in Python when a module, function or feature is no longer recommended and may be removed in a future version of Python. Ignoring deprecation warnings is generally discouraged as it may lead to code that is no longer compatible with future versions of Python. However, in some cases, it may be necessary to suppress these warnings temporarily. In this article, we will discuss some ways to ignore deprecation warnings in Python.

## Using the warnings module

One way to ignore deprecation warnings in Python is to use the `warnings` module. This module provides functions to control how warnings are displayed, including suppressing warnings altogether. The following code demonstrates how to temporarily ignore deprecation warnings:

```
import warnings

with warnings.catch_warnings():
    warnings.filterwarnings("ignore",category=DeprecationWarning)
    # deprecated code goes here
```

The `catch_warnings` function creates a context in which warnings are caught and temporarily suppressed. The `filterwarnings` function is used to specify the types of warnings to ignore. In this case, we are ignoring `DeprecationWarning` warnings.

## Using the -W flag

Another way to ignore deprecation warnings is to use the `-W` flag when running Python. This flag allows you to specify warning categories to ignore from the command line. For example, to ignore `DeprecationWarning` warnings, you can use the following command:

```
python -W ignore::DeprecationWarning myscript.py
```

This will prevent `DeprecationWarning` warnings from being displayed while running `myscript.py`.

## Using the filterwarnings function

The `warnings` module also provides a `filterwarnings` function, which can be used to globally suppress warnings. For example:

```
import warnings
warnings.filterwarnings("ignore", category=DeprecationWarning)
# deprecated code goes here
```

This will suppress all `DeprecationWarning` warnings globally, which may not be desirable. However, it can be useful in certain cases where a large codebase produces many deprecation warnings.

## Conclusion

While ignoring deprecation warnings should generally be avoided, there may be cases where it is necessary to temporarily suppress these warnings. The `warnings` module provides several functions and options for suppressing warnings, including the `catch_warnings` function, the `-W` command line flag, and the `filterwarnings` function. By using these options sparingly and intentionally, you can help ensure that your code remains compatible with future versions of Python.
