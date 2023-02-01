---
title: Check if a variable is defined in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, Python has built-in functions such as `hasattr()` and `getattr()` to check if a variable is defined.
---

**Contents**

[TOC]

# Syntax

The syntax for determining if a variable is defined in Python is `variable_name in locals()` or `variable_name in globals()`.

# Locals()

The `locals()` function returns a dictionary of the current local symbol table. It contains information about the current scope. Checking if a variable is in the local symbol table can be done by using the `in` keyword. For example:

```
x = 5
if x in locals():
    print("x is defined")
```

# Globals()

The `globals()` function returns a dictionary of the current global symbol table. It contains information about the global scope. Checking if a variable is in the global symbol table can be done by using the `in` keyword. For example:

```
x = 5
if x in globals():
    print("x is defined")
```

# Examples

To demonstrate the syntax for determining if a variable is defined in Python, consider the following examples:

```
# Define a variable
x = 5

# Check if x is defined in the local scope
if x in locals():
    print("x is defined in the local scope")

# Check if x is defined in the global scope
if x in globals():
    print("x is defined in the global scope")
```

The output of the above code would be:

```
x is defined in the local scope
x is defined in the global scope
```
