---
title: What is the purpose of functools partial?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Functools partial allows you to create a new function with some of the arguments of an existing function pre-filled.
---

**Contents**

[TOC]

# Overview

The `functools.partial` function allows users to create a new function from an existing function with some of the arguments pre-filled. This is useful for creating functions with fewer arguments, as it allows users to specify certain arguments ahead of time.

# Syntax

The syntax for using `functools.partial` is as follows:

`functools.partial(func, *args, **keywords)`

Where `func` is the existing function to be partially applied, `args` are the positional arguments to be pre-filled, and `keywords` are the keyword arguments to be pre-filled. 

# Usage

To use `functools.partial`, the user must first define the existing function they wish to partially apply. This function can take any number of arguments. For example, the following function takes three arguments:

```
def my_func(a, b, c):
    return a + b + c
```

The user can then create a new function using `functools.partial` by passing in the existing function and any arguments they wish to pre-fill. For example, the following code creates a new function that pre-fills the first argument with the value `1`:

```
from functools import partial
new_func = partial(my_func, 1)
```

The new function, `new_func`, can now be called with two arguments instead of three:

```
new_func(2, 3)
# 6
```

# Conclusion

In summary, `functools.partial` allows users to create a new function from an existing function with some of the arguments pre-filled. This is useful for creating functions with fewer arguments, as it allows users to specify certain arguments ahead of time.
