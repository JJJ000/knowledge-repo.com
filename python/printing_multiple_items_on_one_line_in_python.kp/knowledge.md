---
title: What is the best way to print multiple items (static text and/or variable values) on the same line simultaneously?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the print() function with the end parameter set to an empty string to print multiple things on the same line.
---

**Contents**

[TOC]

**Using String Concatenation:**

1. Create a string that includes the text you want to print.
2. Use the '+' operator to concatenate the strings and values you want to print.
3. Use the `print()` function to print the resulting string.

**Using the `format()` Method:**

1. Create a string that includes the text you want to print and placeholders for the variables you want to print.
2. Use the `format()` method to insert the variables into the string.
3. Use the `print()` function to print the resulting string.

**Using the `f-string` Method:**

1. Create a string that includes the text you want to print and placeholders for the variables you want to print.
2. Use the `f` prefix and the `{}` brackets to insert the variables into the string.
3. Use the `print()` function to print the resulting string.

**Using `str.join()` Method:**

1. Create a list that includes the text you want to print and variables you want to print.
2. Use the `str.join()` method to join the list elements into a single string.
3. Use the `print()` function to print the resulting string.
