---
title: Creating a dictionary using comprehension in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Dictionary Comprehension is a way to create a new dictionary from an existing iterable in a single line of code.
---

**Contents**

[TOC]

## Overview

Dictionary comprehension is a concise and memory-efficient way to create and manipulate dictionaries in Python. It is similar to list comprehension, but it allows you to create a dictionary in one line of code. It is an elegant way to define and create dictionaries by making use of existing iterable objects.

## Syntax

Dictionary comprehension follows the same syntax as list comprehension, with one difference: the expression is followed by a colon (:) and a key-value pair is used to define the elements.

The syntax for dictionary comprehension is as follows:

```
{key:value for (key,value) in iterable}
```

## Examples

Here are some examples of dictionary comprehensions:

```
# Create a dictionary of squares
squares = {x: x**2 for x in range(10)}

# Create a dictionary of strings and their lengths
str_lengths = {key: len(key) for key in ['foo', 'bar', 'baz']}

# Create a dictionary from two lists
keys = ['a', 'b', 'c']
values = [1, 2, 3]
d = {key:value for (key,value) in zip(keys, values)}
```

## Conclusion

Dictionary comprehension is a powerful and efficient way to create and manipulate dictionaries in Python. It is a concise and memory-efficient way to define and create dictionaries by making use of existing iterable objects.
