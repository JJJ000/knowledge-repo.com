---
title: What is the best way to locate all occurrences of a regular expression in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the re.findall() function to find all matches to a regular expression in Python.
---

**Contents**

[TOC]

# Section 1: Using re.findall()
The `re.findall()` function can be used to find all matches to a regular expression in Python. This function takes two arguments: the pattern and the string. It returns a list of all non-overlapping matches of the pattern in the string.

# Section 2: Using re.finditer()
The `re.finditer()` function can also be used to find all matches to a regular expression in Python. This function takes two arguments: the pattern and the string. It returns an iterator object containing all non-overlapping matches of the pattern in the string.

# Section 3: Using re.split()
The `re.split()` function can also be used to find all matches to a regular expression in Python. This function takes two arguments: the pattern and the string. It returns a list of strings that have been split at each match of the pattern in the string.

# Section 4: Using re.sub()
The `re.sub()` function can also be used to find all matches to a regular expression in Python. This function takes three arguments: the pattern, the replacement string, and the string. It returns a copy of the string with all matches of the pattern replaced with the replacement string.
