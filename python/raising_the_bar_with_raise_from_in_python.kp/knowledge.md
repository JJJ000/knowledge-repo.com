---
title: How to use the "raise from" statement in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `raise from` statement allows you to specify an exception to be raised and the exception that caused it.
---

**Contents**

[TOC]

# Introduction

The `raise from` statement in Python is used to raise an exception while preserving the original traceback. This statement can be used to customize the error message and provide additional context to the exception.

# Syntax

The syntax for `raise from` is as follows:

```
raise ExceptionType from OriginalException
```

Where `ExceptionType` is the type of exception to be raised and `OriginalException` is the original exception that occurred and should be preserved in the traceback.

# Example

An example of using the `raise from` statement is as follows:

```
try:
    # Some code here
except Exception as e:
    raise ValueError("Invalid value") from e
```

In this example, a `ValueError` is raised, but the original exception `e` is preserved in the traceback.

# Conclusion

The `raise from` statement is a useful tool for customizing error messages and preserving the original traceback. It should be used when the original exception needs to be preserved in order to provide additional context to the error.
