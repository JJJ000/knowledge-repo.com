---
title: What is the process of verifying whether a string in Python solely consists of numerals?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the isnumeric() method to check if a string contains only numeric characters.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides various ways to check whether a string contains only numbers or not. In this tutorial, we'll discuss some of these methods.

Section 2: Using isnumeric() method
The `isnumeric()` method can be used to check whether a string contains only numeric characters. This method returns True if all characters in the string are numeric, and False otherwise.

Here's an example:

```python
string = "1234"
if string.isnumeric():
    print("String contains only numbers")
else:
    print("String contains other characters as well")
```
Output:

```
String contains only numbers
```

Section 3: Using regular expressions
Python's `re` module provides support for regular expressions. We can use a regular expression to check whether a string contains only numbers.

Here's an example:

```python
import re

string = "1234"
if re.match("^[0-9]+$", string):
    print("String contains only numbers")
else:
    print("String contains other characters as well")
```

Output:

```
String contains only numbers
```

In the above example, we've used the `match()` method of the `re` module to match the regular expression "^[0-9]+$" with the given string. This regular expression matches a string that has one or more digits from 0 to 9.

Section 4: Using try-except block and int() method
Another way to check whether a string contains only numbers is to try to convert it to an integer using the `int()` method. If the conversion is successful, it means that the string contains only numbers. Otherwise, it'll raise a `ValueError` exception.

Here's an example:

```python
string = "1234"
try:
    int(string)
    print("String contains only numbers")
except ValueError:
    print("String contains other characters as well")
```

Output:

```
String contains only numbers
```

In the above example, we've used a `try-except` block to catch the `ValueError` exception that may be raised if the string contains non-numeric characters. If the `int()` method can convert the string to an integer without raising an exception, it means that the string contains only numbers.
