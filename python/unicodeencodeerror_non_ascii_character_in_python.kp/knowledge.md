---
title: The 'ascii' codec cannot process the character u'\xa0' in position 20 because it is not a valid character within the range of 128
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The error occurs when trying to encode a character that is not supported by the specified encoding.
---

**Contents**

[TOC]

# Introduction

The `UnicodeEncodeError` is a common error that occurs when trying to encode a Unicode string in Python. This error occurs when a character in the string is not supported by the specified encoding. In this case, the error occurs when trying to encode a character with the ASCII encoding.

# Explanation

ASCII is an encoding that only supports characters from the English language. It is limited to 128 characters, which are represented by the numbers 0-127. When a character is encountered that is not supported by the ASCII encoding, an error is raised. In this case, the character is the non-breaking space (U+00A0). This character is not supported by the ASCII encoding and thus the error is raised.

# Solution

The solution to this error is to use an encoding that supports the character in question. Unicode is a good choice as it supports all characters, including the non-breaking space. To use Unicode encoding, the `encoding` parameter of the `encode` method must be set to `utf-8`.

# Conclusion

The `UnicodeEncodeError` is a common error that occurs when trying to encode a Unicode string in Python. This error occurs when a character in the string is not supported by the specified encoding. In this case, the character is the non-breaking space (U+00A0), which is not supported by the ASCII encoding. The solution to this error is to use an encoding that supports the character in question, such as Unicode.
