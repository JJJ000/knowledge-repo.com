---
title: Output a string dynamically on one line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Printing in one line in Python can be done by using the `end` argument in the print() function to specify an empty string as the line ending.
---

**Contents**

[TOC]

1. **Using Formatting**

Using the `format()` method, it is possible to print multiple values in a single line. The syntax for this is `print('{} {}'.format(value1, value2))`, where value1 and value2 are the values to be printed.

2. **Using Separator**

The `print()` function also takes an optional argument `sep` which defines the character that is used to separate the values. By default, this is a space. To print multiple values in one line, the syntax is `print(value1, value2, sep='')`.

3. **Using End Argument**

The `print()` function has another optional argument `end` which defines the character that is used to end the line. By default, this is a new line character. To print multiple values in one line, the syntax is `print(value1, value2, end='')`.

4. **Using * Operator**

The `*` operator can be used to unpack a list of values and pass them to the `print()` function. The syntax for this is `print(*values)`, where `values` is a list of values to be printed. This will print the values in the list in one line.
