---
title: Locate the substring in a given string for the nth time
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `find()` method with a starting index to locate the nth occurrence of a substring in a string in Python.
---

**Contents**

[TOC]

## Section 1: Introduction
There are many situations when we have to find the nth occurrence of a substring in a string. There are various ways to achieve this task in Python, and we will be discussing some of them in this article.

## Section 2: Using the re module
The re module provides a method called finditer() that returns an iterator that yields match objects for all the non-overlapping matches of the regular expression in the string. We can use this function to find the nth occurrence of a substring in a string.

```python
import re

def find_nth_occurrence(text, sub_string, n):
    occurrences = [m.start() for m in re.finditer(sub_string, text)]
    if len(occurrences) >= n:
        return occurrences[n-1]
    else:
        return -1
```

In this code, we first use the finditer() method to find all the occurrences of the substring in the text. We store the starting index of each occurrence in a list called occurrences. We then check if there are at least n occurrences of the substring in the text. If there are, we return the starting index of the nth occurrence. Otherwise, we return -1 to indicate that the nth occurrence was not found.

## Section 3: Using the split() method
We can also use the split() method to split the string into substrings at each occurrence of the substring we are looking for. We can then count the number of substrings generated and return the starting index of the nth substring.

```python
def find_nth_occurrence(text, sub_string, n):
    parts = text.split(sub_string, n)
    if len(parts) <= n:
        return -1
    else:
        return len(text) - len(parts[-1]) - len(sub_string)
```

In this code, the split() method takes two arguments, the substring to split the text and the maximum number of splits to make (n). We then count the number of substrings generated and return the starting index of the nth substring.

## Section 4: Conclusion
We have seen two ways to find the nth occurrence of a substring in a string in Python. The first method uses the re module to find all the occurrences of the substring in the text, while the second method uses the split() method to split the text into substrings at each occurrence of the substring. Both methods have their advantages and disadvantages, and the choice of which one to use will depend on the specific requirements of the task at hand.
