---
title: Why does the split() method in Python return an empty list when applied to an empty string, while split('\n') returns ['']?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The default delimiter for split() is any whitespace character, so split() on an empty string results in an empty list, while split(`\n`) on an empty string results in a list with one empty string element since `\n` is treated as a single delimiter.
---

**Contents**

[TOC]

# Explanation: split() function

The split() function in Python is used to divide a string into a list of substrings based on a separator. If the separator is not specified, it splits the string into substrings at any whitespace (spaces, tabs, or newlines). 

# Empty string and the split() function

When the split() function is called on an empty string, it returns an empty list. This is because there are no substrings to split the string by, therefore the resultant list is empty.

# Empty string and the split('\n') function

On the other hand, when the split('\n') function is called on an empty string, it returns a list with one empty string (''). This is because Python treats the empty string as having one element, which is a newline character. Therefore, when using '\n' as the separator in the split() function, Python considers the empty string as having one substrings, which is also an empty string. 

# Conclusion

In summary, split() function returns an empty list when called on an empty string, whereas split('\n') function returns a list with one empty string. This is because Python considers the empty string to have one element, which is a newline character, when using '\n' as the separator.
