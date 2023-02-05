---
title: What is the syntax for creating a function with optional parameters?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, a function can be defined with optional arguments by specifying default values for the arguments in the function definition.
---

**Contents**

[TOC]

#### Syntax

The syntax for defining a function with optional arguments in Python is:

```
def function_name(arg1, arg2=default_value):
    # function body
```

#### Example

For example, the following function takes two arguments, one of which is optional and has a default value:

```
def add(a, b=1):
    return a + b
```

#### Usage

The function can be called with either one or two arguments. When two arguments are provided, the second argument will override the default value.

```
add(2) # returns 3 (2 + 1)
add(2, 3) # returns 5 (2 + 3)
```

#### Benefits

Using optional arguments can make functions more versatile and easier to use. It also allows the function to be called with fewer arguments, which can be useful if the user does not need to provide all of the arguments.
