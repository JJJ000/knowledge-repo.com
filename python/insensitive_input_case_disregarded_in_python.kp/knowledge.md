---
title: Not sensitive to case
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The `in` keyword in Python is case-sensitive by default, but can be made case-insensitive by converting both the target string and search string to lowercase using the `lower()` method.
---

**Contents**

[TOC]

Introduction
------------
In Python, we can use 'in' to check whether a substring is present in a string or not. However, this operation is case-sensitive, which means it distinguishes between uppercase and lowercase letters. For example, if we use 'in' to check for the string 'hello' in the string 'Hello, world!', it will return false. In this article, we will discuss different ways to use 'in' case-insensitively in Python.

Using str.lower() Method
-------------------------
The simplest way to use 'in' case-insensitively is by converting both the substring and the string to lowercase using the str.lower() method. This method returns a lowercase copy of the string. Here's an example:

string = 'Hello, world!'
substring = 'hello'

if substring.lower() in string.lower():
    print(substring, 'is present in', string)
else:
    print(substring, 'is not present in', string)

Output:
hello is present in Hello, world!

Using re Module
----------------
Another way to use 'in' case-insensitively is by using the re module in Python. We can use the search() method of the re module with the re.IGNORECASE flag to perform a case-insensitive search. Here's an example:

import re

string = 'Hello, world!'
substring = 'hello'

if re.search(substring, string, re.IGNORECASE):
    print(substring, 'is present in', string)
else:
    print(substring, 'is not present in', string)

Output:
hello is present in Hello, world!

Using str.lower() Method with lambda Function in filter()
-----------------------------------------------------------
We can also use the str.lower() method and lambda function with the filter() function to get all the case-insensitive occurrences of a substring in a string. Here's an example:

string = 'Hello, World!Hello, World!'
substring = 'hello'

occurrences = list(filter(lambda x: substring.lower() in x.lower(), string.split()))

print(substring, 'occurs', len(occurrences), 'times in', string)

Output:
hello occurs 2 times in Hello, World!Hello, World!

Conclusion
----------
In this article, we have discussed different ways to use 'in' case-insensitively in Python, such as using the str.lower() method, the re module, and the filter() function with a lambda function. These methods are useful in cases where we need to perform case-insensitive string operations in our Python code.
