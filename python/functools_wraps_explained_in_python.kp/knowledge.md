---
title: What is the purpose of the functools.wraps function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Functools.wraps is a decorator used to preserve the original metadata of a wrapped function, such as its name, docstring, and arguments list.
---

**Contents**

[TOC]

### What is functools.wraps?

functools.wraps is a decorator that is used to wrap a function in order to preserve its metadata. This enables the wrapped function to have the same name, docstring, and other attributes as the original function.

### How Does It Work?

functools.wraps works by taking the original function as an argument and creating a new function that wraps the original. The new function is then assigned the same name, docstring, and other attributes as the original.

### Benefits of Using functools.wraps

Using functools.wraps can make debugging easier, as it preserves the original function's metadata. It also makes it easier to read and understand code, as the original function's name and other attributes are preserved. Additionally, it can make code more maintainable, as the original function's name and other attributes are preserved.

### Limitations of Using functools.wraps

Although functools.wraps can be useful, it can also be limiting in certain scenarios. For example, if the original function is modified, the wrapped function will not reflect the changes. Additionally, if the original function has any side effects, they will not be reflected in the wrapped function.
