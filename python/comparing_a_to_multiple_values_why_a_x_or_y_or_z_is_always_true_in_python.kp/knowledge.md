---
title: How can I compare "a" to the values x, y, and z all at once, and why does the expression "a == x or y or z" always give a true result?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: In Python, `a == x or y or z` always evaluates to True because the boolean operation `or` returns the first truthy value it encounters between `x`, `y`, and `z`, and to compare `a` to all of those values separately, you should use `a in [x, y, z]`.
---

**Contents**

[TOC]

# Understanding the Evaluation of "a == x or y or z"

When we write `a == x or y or z` in Python, what happens is that the interpreter evaluates the expression from left to right, as follows:

1. `a == x` is evaluated first. If this is `True`, then the entire expression is `True` and the interpreter stops evaluating.
2. If `a == x` is `False`, then the interpreter moves on to the next part, which is `y`. Since `y` is a non-empty string in this case, it is considered `True` and the interpreter doesn't even evaluate the expression `y or z`. Therefore, the entire expression `a == x or y or z` is `True`.


# Using Comparison Operators to Compare "a" to All Values

If we want to compare `a` to all of the values `x`, `y`, and `z`, we need to use comparison operators for each comparison. Here's an example:

```
if a == x or a == y or a == z:
    # do something
```

This code will check if `a` is equal to any of the values `x`, `y`, or `z` using the `==` operator, and execute the code inside the `if` block only if the condition is `True`. If you have many values to compare, this approach can become unwieldy, so you might want to consider other options.


# Using Lists to Check if "a" is in a Collection of Values

One approach to simplifying the comparison of `a` to multiple values is to use a list or tuple to store the values, and use the `in` operator to check if `a` is in the collection. Here's an example:

```
values = [x, y, z]
if a in values:
    # do something
```

This code will create a list `values` containing the values `x`, `y`, and `z`, and then check if `a` is in the list using the `in` operator. If `a` is in the list, the code inside the `if` block will execute.


# Using Sets to Check if "a" is in a Collection of Unique Values

If you want to check if `a` is in a collection of unique values (`x`, `y`, and `z` are all unique), you can use a set instead of a list or tuple. Sets are collections of unique elements, so you can use the `in` operator to check if an element is in the set. Here's an example:

```
values = {x, y, z}
if a in values:
    # do something
```

This code will create a set `values` containing the values `x`, `y`, and `z`, and then check if `a` is in the set using the `in` operator. If `a` is in the set, the code inside the `if` block will execute. Using a set instead of a list or tuple can improve performance if you have many unique values to compare.
