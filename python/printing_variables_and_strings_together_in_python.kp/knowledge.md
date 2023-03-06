---
title: What is the method to print a variable and a string together on a single line using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the string concatenation operator (+) to combine the variable and string, then use the print function to output them on the same line.
---

**Contents**

[TOC]

Section 1: Introduction 
In Python, printing a variable and a string on the same line can be achieved by concatenating the variable with the string using the '+' operator. There are also other ways to achieve this. This tutorial will show how to print a variable and string on the same line in Python.

Section 2: Using the "+" Operator 
The easiest way to print a variable and string on the same line in Python is by using the '+' operator to concatenate the two values. Here's an example:

```
var = "world"
print("Hello " + var)
```

Output:
```
Hello world
```

In the example above, we have a string "Hello " and a variable “var” that contains the string "world". The '+' operator is used to concatenate the two values and output them on the same line.

Section 3: Using the "{}" Placeholder 
Another way to print a variable and string on the same line in Python is by using the "{}" placeholder. Here's an example:

```
var = "world"
print("Hello {}".format(var))
```

Output:
```
Hello world
```

In the example above, we have a string "Hello " and a variable “var” that contains the string "world". The "{}" placeholder is used to indicate where the value of "var" should be inserted in the string. The format() method is then used to replace the placeholder with the actual value of "var".

Section 4: Using F-Strings 
Python 3.6 introduced a new feature called f-strings that makes it even easier to print a variable and string on the same line. Here's an example:

```
var = "world"
print(f"Hello {var}")
```

Output:
```
Hello world
```

In the example above, we have a string "Hello " and a variable “var” that contains the string "world". The f-string is used to embed the value of "var" directly in the string by placing the variable name inside curly braces {}. The f-string also allows us to mix expressions with curly braces {}.

This concludes this tutorial on how to print a variable and string on the same line in Python. Go ahead and use any of the outlined ways to print a variable and string on the same line in your Python projects.
