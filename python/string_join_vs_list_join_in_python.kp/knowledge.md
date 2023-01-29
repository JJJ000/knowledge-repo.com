---
title: Why does the string.join() method take a list as an argument instead of the list.join() method taking a string as an argument?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Python`s string.join() method joins the elements of an iterable (such as a list) to a string, using the string as a separator, whereas list.join() does not exist.
---

**Contents**

[TOC]

### 1. Historical Reason

Python's `string.join()` method is based on the `str.join()` method from the string module in Python 2, which was released in 2000. At the time, there was no concept of a `list.join()` method.

### 2. Syntax

The syntax of `string.join()` makes more sense in the context of joining multiple strings together. By joining a list with a string, the string acts as a separator between the elements of the list, and the result is a single string.

### 3. Functionality

The `string.join()` method is more versatile than `list.join()` would be. `string.join()` can be used to join any iterable object, such as a list, tuple, or dictionary. On the other hand, `list.join()` would only be able to join lists.

### 4. Popularity

Since its introduction, the `string.join()` method has become a popular way to join strings together, and is now widely used in Python code.
