---
title: One way to format strings in Python using several arguments is to use the syntax of '%s ... %s'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The syntax for using multiple arguments for string formatting in Python is to use the % operator with the appropriate number and type of placeholders separated by commas.
---

**Contents**

[TOC]

Section 1: Introduction
String formatting is a process of substituting one or more values in a string with respective arguments. Python offers multiple ways of string formatting including string interpolation, format string method, and f-strings. In this article, we will specifically focus on using multiple arguments for string formatting in Python using the format string method.

Section 2: String Formatting with Multiple Arguments
To use multiple arguments in string formatting, we need to pass the values in a tuple or a list. Each argument corresponds to the respective placeholder in the string. The placeholders are represented with curly braces ('{}'). Let's take an example:

```
>>> name = 'John'
>>> age = 30
>>> print('My name is {} and I am {} years old.'.format(name, age))
My name is John and I am 30 years old.
```

In the above example, we have two variables 'name' and 'age' that are passed as arguments to the string using format method. The values are substituted in respective curly braces.

Section 3: Using Named Arguments
We can also use named arguments in string formatting. We need to use the keyword arguments in the format method along with the respective placeholder names. Let's see an example:

```
>>> name = 'John'
>>> age = 30
>>> print('My name is {nm} and I am {a} years old.'.format(nm=name, a=age))
My name is John and I am 30 years old.
```

In the above example, we have used named arguments 'nm' for 'name' and 'a' for 'age'.

Section 4: Using Format Specifiers
We can also use format specifiers to format the string output. Format specifiers are used to control the display of values in the output string. Let's see an example:

```
>>> num = 3.14159265359
>>> print('The value of pi is {:.2f}'.format(num))
The value of pi is 3.14
```

In the above example, we have used a format specifier '{:.2f}' to round off the value of 'num' up to two decimal places.

Conclusion:
In this article, we learned how to use multiple arguments in string formatting in Python using the format method. We also learned how to use named arguments and format specifiers for more control over the output. String formatting is an essential concept in Python and can be useful in a variety of applications.
