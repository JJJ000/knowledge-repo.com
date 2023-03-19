---
title: A 'typeerror' occurred where a string pattern cannot be applied to a bytes-like object during the execution of re.findall()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: This error occurs when using a bytes-like object (e.g. a binary file) with a regular expression pattern that expects a string input in the re.findall() method.
---

**Contents**

[TOC]

Section 1: Background

The `re` module in Python is the built-in module for regular expressions. It allows us to search for patterns in strings using regular expressions. Regular expressions are a powerful tool that can help us parse and analyze text data.

The `findall()` method is one of the most commonly used methods in the `re` module. It searches for all occurrences of a pattern in a string and returns a list of all matching substrings.

Section 2: Error message

The `TypeError: can't use a string pattern on a bytes-like object` error message is raised when we try to use a string pattern on a bytes-like object in `re.findall()` method. Bytes-like objects are objects that behave like bytes, such as byte strings or byte arrays. A string pattern is a regular expression pattern defined as a Python string.

Section 3: Solution

To solve this error, we can use a byte string pattern instead of a string pattern. A byte string pattern is a regular expression pattern defined as a bytes object instead of a Python string.

Example:

```python
import re

text = b'The quick brown fox jumps over the lazy dog'
pattern = b'\w+'

matches = re.findall(pattern, text)
print(matches)
```

Output:

```
[b'The', b'quick', b'brown', b'fox', b'jumps', b'over', b'the', b'lazy', b'dog']
```

In this example, we defined the `text` variable as a byte string and the `pattern` variable as a byte string pattern. We used the `re.findall()` method to find all occurrences of the pattern in the text and returned a list of all matching byte strings.

Section 4: Conclusion

In conclusion, the `TypeError: can't use a string pattern on a bytes-like object` error is raised when we try to use a string pattern on a bytes-like object in `re.findall()` method. To solve this error, we can use a byte string pattern instead of a string pattern.
