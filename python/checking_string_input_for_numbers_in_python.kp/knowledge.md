---
title: What is the way to verify if an input string is a numerical value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the isnumeric() method to check if a string input is a number in Python.
---

**Contents**

[TOC]

Section 1: Introduction
To check if the string input is a number in Python, there are several methods that can be used. This can be done using built-in methods or regular expressions. Furthermore, we need to determine what type of number we are checking for - integers, floats, or a combination of both.

Section 2: Using built-in methods
There are several built-in methods in Python that can be used to check whether a given string is numeric. One of these methods is the isnumeric() method. This method checks whether all the characters in the given string are numeric, and it returns true if this is the case. Another method is isdigit(), which is similar to isnumeric() but only considers digits 0-9. These methods can be useful when checking for integers.

```
num = "123"
if num.isnumeric():
    print("This is a number")
else:
    print("This is not a number")
```

Similarly, for float numbers, we can use the isfloat() function by converting the input string into float.

```
num = "123.45"
try:
    float(num)
    print("This is a floating-point number")
except ValueError:
    print("This is not a number")
```

Section 3: Using regular expressions
Regular expressions can be used to check whether a given string is numeric. This is particularly useful when checking for complex numbers or numbers that contain specific formatting requirements. For example, we can use the re module to define a regular expression that matches any valid floating-point number. We can then use this regular expression to test whether a given string is a valid floating-point number.

```
import re

num_regex = "^[-+]?[0-9]*\.?[0-9]+([eE][-+]?[0-9]+)?$"
num = "123.45"
if re.match(num_regex, num):
    print("This is a valid floating-point number")
else:
    print("This is not a valid floating-point number")
```

Section 4: Conclusion
In conclusion, there are several methods available to check whether a given string is a number in Python. Built-in methods can be simple and efficient when checking for integers and floats. Regular expressions can be used for more complex numbers that require specific formatting requirements. When it comes to checking for numbers in Python, the method used will depend on the specific use case and the type of number being checked.
