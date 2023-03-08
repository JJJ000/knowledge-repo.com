---
title: How to convert unicode to ascii in Python without encountering any errors?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Unicode can be converted to ASCII without errors in Python using the unicodedata module`s normalize function to convert Unicode characters to their closest ASCII equivalent.
---

**Contents**

[TOC]

# Introduction

Unicode is a universal encoding standard that represents all the characters used in different languages and scripts. ASCII, on the other hand, is an older encoding standard that represents only the characters used in the English language. Sometimes, we may need to convert Unicode to ASCII for various purposes, such as database storage or text analysis. However, there can be errors while converting Unicode to ASCII because not all Unicode characters can be represented in ASCII. In this article, we will discuss how to convert Unicode to ASCII without errors in Python.

# Method 1: Using the Unidecode Library

The Unidecode library provides a simple solution for converting Unicode to ASCII without errors. The library includes a function called `unidecode` that takes a Unicode string as input and returns an ASCII string. The function replaces non-ASCII characters with their ASCII equivalents or removes them if no ASCII equivalent exists.

```
# Importing the Unidecode library
from unidecode import unidecode

# Converting a Unicode string to ASCII
unicode_string = "Café"
ascii_string = unidecode(unicode_string)

# Printing the output
print(ascii_string)  # Output: Cafe
```

# Method 2: Using the encode Function with the "ascii" Parameter

Python's built-in `encode` function can also be used to convert Unicode to ASCII. We can pass the "ascii" parameter to the `encode` function to restrict the output to ASCII characters only. If there are any non-ASCII characters, the `encode` function will raise a `UnicodeEncodeError`. To handle this error, we can use the `replace` parameter to replace non-ASCII characters with "?" or an empty string.

```
# Converting a Unicode string to ASCII
unicode_string = "Café"
ascii_string = unicode_string.encode("ascii", "replace").decode()

# Printing the output
print(ascii_string)  # Output: Cafe
```

# Method 3: Using the normalize Function with the "NFKD" Form

Another way to convert Unicode to ASCII is to use Python's built-in `normalize` function with the "NFKD" form. This form decomposes combined characters into their constituent parts and represents them as separate characters. We can then remove the non-ASCII characters using the `encode` function with the "ascii" parameter.

```
# Converting a Unicode string to ASCII
import unicodedata

unicode_string = "Café"
ascii_string = unicodedata.normalize("NFKD", unicode_string).encode("ascii", "ignore").decode()

# Printing the output
print(ascii_string)  # Output: Cafe
```

# Conclusion

In this article, we have discussed three methods for converting Unicode to ASCII without errors in Python. We can use the Unidecode library, the `encode` function with the "ascii" parameter, or the `normalize` function with the "NFKD" form. Each method has its pros and cons, depending on the specific requirements of the task.
