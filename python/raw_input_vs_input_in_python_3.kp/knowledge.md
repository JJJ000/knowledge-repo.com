---
title: What are the distinctions between using "raw_input()" and "input()" in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: `raw\_input()` is used in Python 2 and is equivalent to `input()` in Python 3, which evaluates the input as an expression.
---

**Contents**

[TOC]

### `raw_input()`
`raw_input()` is a function in Python 2.x that takes a string as an argument and returns the string with the trailing newline stripped.

### `input()`
`input()` is a function in Python 3.x that takes a string as an argument and evaluates the string as a Python expression.

### Differences
The main difference between `raw_input()` and `input()` is that `input()` evaluates the string as a Python expression, while `raw_input()` does not. This means that `input()` can be used to evaluate mathematical expressions, while `raw_input()` cannot. Additionally, `input()` will raise an error if the input string is not valid Python code, while `raw_input()` will not.
