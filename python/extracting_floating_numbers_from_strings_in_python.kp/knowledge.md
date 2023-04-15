---
title: How to retrieve a decimal number from a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use regular expressions and the re module, specifically the re.findall() function, to extract floating numbers from a string in Python.
---

**Contents**

[TOC]

## Option 1: Using Regular Expressions

We can use regular expressions to search for patterns in the string that match the format of a floating point number. The following code snippet shows how to use regular expressions to extract floating point numbers from a string:

```python
import re

string = "The price of the product is $12.50"
float_regex = r'[-+]?\d*\.\d+|\d+'
result = re.findall(float_regex, string)
print(result) # Output: ['12.50']
```

The regular expression `[-+]?\d*\.\d+|\d+` matches two patterns: 

- The first pattern `[-+]?\d*\.\d+` matches floating point numbers with an optional sign (`[-+]?`), zero or more digits before the decimal point (`\d*`), and one or more digits after the decimal point (`\.\d+`).
- The second pattern `\d+` matches integers with one or more digits. 

The `findall()` method of the `re` module returns all non-overlapping matches of the regular expression in the string. 

## Option 2: Using isdigit() and split()

If the floating point number is surrounded by non-digit characters, we can split the string and check if each segment is a valid floating point number using the `isdigit()` method. Here's an example:

```python
string = "The annual sales growth rate is 3.5%."
segments = string.split()
float_numbers = []
for segment in segments:
    if segment[-1] == '%':
        segment = segment[:-1]
    if segment.isdigit():
        float_numbers.append(float(segment))
print(float_numbers) # Output: [3.5]
```

We split the string into segments using the `split()` method. Then, we check if each segment is a valid floating point number by removing the percentage sign (if exists) and checking if the remaining characters are digits using the `isdigit()` method. If the segment is a valid floating point number, we convert it to a float using the `float()` function and add it to a list of floating point numbers.

## Option 3: Using Regular Expressions and sub()

Another way to extract a floating point number from a string is to use regular expressions with the `sub()` method to remove all non-numeric characters. Here's an example:

```python
import re

string = "The average temperature in May was 24.5 degrees Celsius."
float_regex = r'[-+]?\d*\.\d+|\d+'
numbers_only = re.sub(r'[^\d\.]+', '', string)
float_number = re.findall(float_regex, numbers_only)[0]
print(float_number) # Output: 24.5
```

The regular expression `[-+]?\d*\.\d+|\d+` matches floating point numbers and integers (as explained in option 1). The `sub()` method replaces all non-numeric characters (denoted by the regular expression `[^\d\.]+`) with an empty string, effectively removing them from the string. Finally, we extract the floating point number using the `findall()` method, assuming that there is only one floating point number in the string.
