---
title: Comparing the usage of eval() to ast.literal_eval() in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: eval() can execute any arbitrary code, while ast.literal\_eval() can only evaluate a subset of Python expressions safely.
---

**Contents**

[TOC]

Introduction
------------

Python provides a couple of useful built-in functions for evaluating strings as code or expressions. These functions are `eval()` and `ast.literal_eval()`. While both functions take input strings, they have different use cases and levels of security.

`eval()` vs `ast.literal_eval()`
-------------------------------

`eval()` and `ast.literal_eval()` both evaluate strings as code or expressions, but `eval()` can execute any Python code, including executable statements, while `ast.literal_eval()` can only evaluate literals, such as strings, numbers, tuples, lists, dicts, and booleans.

This means that `eval()` can be dangerous if the input string comes from an untrusted source, such as user input, as it can execute arbitrary code, including malicious code. This can lead to security vulnerabilities, such as code injection attacks.

On the other hand, `ast.literal_eval()` is safe to use with untrusted input, as it only evaluates literals and does not execute any code or statements. This makes it useful for tasks such as safely evaluating configuration files, parsing command-line arguments, or decoding JSON data.

Examples
--------

Here is an example of using `eval()`:

```python
a = 1
b = 2
c = eval("a + b")
print(c)  # Output: 3
```

As you can see, `eval()` takes a string containing code and evaluates it as if it were normal Python code.

Here is an example of using `ast.literal_eval()`:

```python
import ast

s = '"Hello, World!"'
s_evaluated = ast.literal_eval(s)
print(s_evaluated)  # Output: Hello, World!
```

In this example, `ast.literal_eval()` takes a string containing a string literal and evaluates it as a string. Since the input is a literal, it is safe to use `ast.literal_eval()`.
