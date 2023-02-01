---
title: What is the process for creating variables that can change?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python, variable variables can be created by assigning a variable name to the value of another variable.
---

**Contents**

[TOC]

# Section 1: Understanding Variable Variables
Variable variables are variables whose names are determined by the value of another variable. This means that the name of the variable is not predetermined, but rather is determined at run-time based on the value of another variable.

# Section 2: Creating Variable Variables
In Python, variable variables can be created by using the `globals()` or `locals()` functions. The `globals()` function returns a dictionary of all global variables, while the `locals()` function returns a dictionary of all local variables. The dictionary can then be used to access the value of a variable based on the value of another variable.

# Section 3: Example
For example, if we have a variable `name` with the value "foo", we can use the `globals()` function to access the value of the variable `foo`:

```
name = "foo"
foo = "bar"

print(globals()[name]) # prints "bar"
```

# Section 4: Further Reading
For more information on variable variables in Python, see the official Python documentation [here](https://docs.python.org/3/faq/programming.html#how-do-i-create-a-variable-number-of-variables).
