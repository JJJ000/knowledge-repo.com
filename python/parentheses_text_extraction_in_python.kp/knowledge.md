---
title: Reworded how to write a regular expression that extracts the text enclosed within parentheses?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The regular expression is `\((.*?)\)` where `?` signifies non-greedy matching and `.*?` matches any character (except newline) zero or more times.
---

**Contents**

[TOC]

Section 1: Introduction
Regular expressions are powerful tools that allow us to search and manipulate text data. In Python, we can use regular expressions with the `re` module. In this tutorial, we will explore the regular expression that returns text between parenthesis.

Section 2: Creating the regular expression
To create the regular expression, we need to use parentheses `()` to match the opening and closing parenthesis. We will use the `re.search()` method to search for the pattern in a string.

Here is the regular expression:
```python
import re

text = "This is some (text) with (parentheses)"
pattern = r'\((.*?)\)'
results = re.findall(pattern, text)
print(results)
```
Output:
```
['text', 'parentheses']
```

Section 3: Explanation of regular expression
The regular expression has three parts:
1. An opening parenthesis `\(` to match the opening parenthesis in the text.
2. A capturing group `(.*?)` which matches zero or more characters of any type between the opening and closing parenthesis.
3. A closing parenthesis `\)` to match the closing parenthesis in the text.

The `*?` in the capturing group makes it non-greedy, which means it will match the smallest possible string between the opening and closing parenthesis.

Section 4: Conclusion
In this tutorial, we learned how to use regular expressions in Python to return text between parenthesis. We also explored the regular expression pattern and its explanation.
