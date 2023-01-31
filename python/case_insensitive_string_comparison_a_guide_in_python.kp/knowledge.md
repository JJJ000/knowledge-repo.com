---
title: What is the best way to compare strings without differentiating between upper and lower case letters?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the str.casefold() method to compare two strings in a case-insensitive manner.
---

**Contents**

[TOC]

# Using the == Operator
The == operator can be used to compare two strings in a case-insensitive manner. This is done by converting both strings to the same case (upper or lower) before performing the comparison.

# Using the str.casefold() Method
The str.casefold() method can be used to compare two strings in a case-insensitive manner. This method returns a casefolded string which can be compared with the other string.

# Using the str.lower() Method
The str.lower() method can be used to compare two strings in a case-insensitive manner. This method returns a lowercase string which can be compared with the other string.

# Using the str.upper() Method
The str.upper() method can be used to compare two strings in a case-insensitive manner. This method returns an uppercase string which can be compared with the other string.
