---
title: The value provided cannot be converted to an integer in base 10
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: An empty string is not a valid literal for int() in Python.
---

**Contents**

[TOC]

# Explanation

When attempting to convert a string to an integer, Python will raise a `ValueError` if the string is empty. This is because the empty string cannot be converted to an integer.

# Causes

The most common cause of this error is attempting to convert a string that does not contain a valid integer. This could be due to the string containing non-numeric characters, or due to the string being empty.

# Solutions

The best way to solve this error is to check the string before attempting to convert it to an integer. If the string is empty, it can be handled appropriately. If the string contains non-numeric characters, they can be removed before attempting to convert the string to an integer.
