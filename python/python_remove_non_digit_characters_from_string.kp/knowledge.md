---
title: How can we use Python to eliminate all non-digit characters from a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: We can use the regular expression module re and the method sub to remove all characters except digits from a string in Python.
---

**Contents**

[TOC]

## Introduction

Python provides various ways to manipulate strings. In this tutorial, we will discuss how to remove characters except digits from a string in Python. 

## Using Regular Expression

Python provides `re` module for regular expression operations. The regular expression `[^0-9]` will match any character except digits. We can use `re.sub()` function to replace those characters with an empty string.

```python
import re

string = "Hello123World!"

result = re.sub('[^0-9]', '', string)

print(result) # Output: 123
```

In this example, we imported `re` module, defined the input string, and used `re.sub()` to replace all non-digit characters with an empty string.

## Using isdigit() method

Python's `isdigit()` method can be used to check if a character is a digit or not. We can loop through the string characters, keep the digits, and discard the non-digit characters.

```python
string = "Hello123World!"

result = ""

for char in string:
    if char.isdigit():
        result += char

print(result) # Output: 123
```

In this example, we looped through the characters of the `string`, used `isdigit()` method to check if the character is a digit or not, and kept the digit characters in the `result` string.

## Using filter() and lambda function

Python's `filter()` function can be used to filter out elements from an iterable. We can use a lambda function to filter out only the digit characters from the input string.

```python
string = "Hello123World!"

result = "".join(filter(lambda x: x.isdigit(), string))

print(result) # Output: 123
```

In this example, we used `filter()` function to filter out only the digit characters, and `"".join()` to convert the resulting filter object into a string.

## Conclusion

In this tutorial, we discussed three methods to remove characters except digits from a string in Python. You can choose any method that fits your situation and requirements.
