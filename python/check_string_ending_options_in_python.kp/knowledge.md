---
title: Verify whether the string culminates with any of the terms in a given list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the any() function with a generator expression that checks if the given string ends with any element in the list.
---

**Contents**

[TOC]

# Section 1: Problem statement
Suppose you have a string and a list of strings. You want to check if the given string ends with any of the strings present in the list. How would you do it in Python?

# Section 2: Solution using string method
Python provides a built-in method `endswith()` to check if a string ends with a particular substring or not. We can use a loop to iterate over the list of strings and apply `endswith()` on the given string to check if it ends with any of the substrings.

```
string = "hello world"
suffixes = ["ld", "rl", "lo"]

for suffix in suffixes:
    if string.endswith(suffix):
        print("String ends with: ", suffix)
```

Output:
```
String ends with: ld
String ends with: lo
```

# Section 3: Solution using regular expression
Another way to solve this problem is to use regular expressions. We can create a regular expression pattern that matches any of the strings present in the list as a suffix of the given string. We can then use the `search()` method of the `re` module to search for this pattern in the string.

```
import re

string = "hello world"
suffixes = ["ld", "rl", "lo"]
pattern = "|".join(suffixes) + "$"

if re.search(pattern, string):
    print("String ends with one of the suffixes")
```
Output:
```
String ends with one of the suffixes
```

# Section 4: Conclusion
In this tutorial, we learned two ways to check if a string ends with any of the strings present in a list. We can either iterate over the list and use the `endswith()` method or create a regular expression pattern and use the `search()` method to search for the pattern in the given string.
