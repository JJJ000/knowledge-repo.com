---
title: Comparison of generator expressions and list comprehensions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Generator expressions are used to create iterators, while list comprehensions are used to create lists.
---

**Contents**

[TOC]

# Generator Expressions

Generator expressions are a type of generator that are written in a similar way to list comprehensions. They are similar to list comprehensions, but instead of returning a list, they return a generator object. This means that they can be used to create iterators that generate values on the fly instead of storing them in a list.

# List Comprehensions

List comprehensions are a type of looping construct that is used to create lists from existing iterables. List comprehensions use the same syntax as generator expressions, but instead of returning a generator object, they return a list. This makes them useful for creating lists of values from existing data.

# Difference

The main difference between generator expressions and list comprehensions is that generator expressions are used to create iterators that generate values on the fly, while list comprehensions are used to create lists of values from existing data. Generator expressions are more efficient than list comprehensions, since they don't have to store the values in a list, but list comprehensions are more versatile since they can be used to create more complex lists.
