---
title: Printing without a newline or space
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Print with the end argument set to an empty string print(`Hello`, end=``)
---

**Contents**

[TOC]

# Section 1: Using the Print Function

The print function in Python can be used to print without a newline or space by adding an argument to the print function. The argument is called `end` and can be used to specify what character should be printed at the end of the line. By default, the `end` argument is set to `\n` which means a newline character will be printed at the end of the line. To print without a newline, the `end` argument should be set to an empty string `''`.

# Section 2: Using the sys.stdout.write Function

The `sys.stdout.write` function can be used to print without a newline or space. This function does not automatically add a newline character to the end of the line, so no additional arguments are needed.

# Section 3: Using the print Function with the Separator Argument

The print function also allows the use of a `sep` argument which specifies the character that should be printed between the values. By default, the `sep` argument is set to `' '` which means a space will be printed between the values. To print without a space, the `sep` argument should be set to an empty string `''`.

# Section 4: Using the String Formatting Method

The string formatting method can also be used to print without a newline or space. This method involves using the `%` operator to specify the values that should be printed and the `end` argument to specify what character should be printed at the end of the line. By default, the `end` argument is set to `\n` which means a newline character will be printed at the end of the line. To print without a newline, the `end` argument should be set to an empty string `''`.
