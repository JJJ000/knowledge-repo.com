---
title: Comparing '%', '.format' and 'f-string literal' approaches to string formatting
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The % formatting is the oldest way to format strings in Python, the .format method is a more modern way to do string formatting, and f-string literals are the newest and most powerful way to format strings in Python.
---

**Contents**

[TOC]

## % Formatting

The `%` operator is used for string formatting in Python. It is the oldest method of formatting strings in Python and is also known as the string formatting operator. The `%` operator works by substituting a value or expression for a placeholder in a string. The placeholder is usually denoted by a `%` character followed by a single letter or a number.

For example:

`name = "John"`

`print("Hello %s!" % name)`

The output of this code would be:

`Hello John!`

## .format()

The `.format()` method is a newer and more powerful way of formatting strings in Python. It is a method of the `str` class and can be used to format strings in various ways. It works by substituting values or expressions for placeholders in a string. The placeholder is denoted by curly braces `{}` and can contain a number, a keyword, or a combination of both.

For example:

`name = "John"`

`print("Hello {0}!".format(name))`

The output of this code would be:

`Hello John!`

## f-string literal

The f-string literal is a new way of formatting strings in Python introduced in Python 3.6. It is a method of the `str` class and works by substituting values or expressions for placeholders in a string. The placeholder is denoted by an `f` character followed by curly braces `{}` and can contain a number, a keyword, or a combination of both.

For example:

`name = "John"`

`print(f"Hello {name}!")`

The output of this code would be:

`Hello John!`
