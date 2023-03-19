---
title: Raise an exception with modified type and message while retaining the existing details
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To re-raise an exception with a different type and message while preserving existing information, use the `raise` statement with the new type and message inside the `except` block followed by the `from` keyword and the original exception.
---

**Contents**

[TOC]

### Section 1: Introduction

In Python, sometimes it is necessary to handle an exception that has already occurred, and re-raise it with a different type and message while preserving the existing information of the exception. This can be useful for debugging, error reporting, and customizing error messages for specific use cases. In this tutorial, we will explore how to do that.

### Section 2: Handling an exception and re-raising it with a different type

One way to handle an exception and re-raise it with a different type is to use the `raise` statement with a new exception class and an optional error message. Here is an example:

```python
try:
    # some code that may raise an exception
except ValueError as ve:
    raise TypeError("Invalid type") from ve
```

In this example, if a `ValueError` occurs inside the `try` block, we catch it and re-raise it as a `TypeError` with a new error message, while preserving the original exception information using the `from` keyword.

### Section 3: Preserving the existing information

To preserve the existing information of an exception while re-raising it with a different type and message, we can use the `raise` statement with the `from` keyword to chain exceptions. Here is an example:

```python
try:
    # some code that may raise an exception
except ValueError as ve:
    raise TypeError("Invalid type") from ve
```

In this example, if a `ValueError` occurs inside the `try` block, we catch it and re-raise it as a `TypeError` with a new error message, while preserving the original exception information using the `from` keyword.

### Section 4: Conclusion

In conclusion, handling an exception and re-raising it with a different type and message while preserving the existing information of the exception can be done by using the `raise` statement with a new exception class and an optional error message, with the `from` keyword to chain exceptions. This approach provides a powerful way to customize error messages for specific use cases and improve the readability of error messages.
