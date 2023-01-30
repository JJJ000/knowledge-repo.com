---
title: Change a string version of a dictionary into a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the built-in function eval() to convert a string representation of a dictionary to a dictionary in Python.
---

**Contents**

[TOC]

**Section 1: Parse the String**

The first step is to parse the string representation of the dictionary into a valid Python dictionary. This can be done using the `ast.literal_eval` method. This method will evaluate the string and return a Python dictionary object.

**Section 2: Set up the String**

Before the string can be parsed, it must be set up in the correct format. This means that each key-value pair must be separated by a comma, and the entire dictionary must be surrounded by curly braces.

**Section 3: Evaluate the String**

Once the string is properly formatted, it can be evaluated using the `ast.literal_eval` method. This method takes the string as an argument and returns a Python dictionary object.

**Section 4: Access the Dictionary**

Once the string has been evaluated, the resulting dictionary can be accessed using standard dictionary methods. For example, the `get()` method can be used to retrieve the value associated with a particular key.
