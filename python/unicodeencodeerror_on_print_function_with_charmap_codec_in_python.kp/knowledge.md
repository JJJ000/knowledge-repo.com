---
title: The print function is encountering a unicodeencodeerror with the 'charmap' codec, indicating that it is unable to encode a character that maps to an undefined value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: This error occurs when you try to print or write a character that cannot be encoded using the default encoding of your system.
---

**Contents**

[TOC]

## Overview

The `UnicodeEncodeError: 'charmap' codec can't encode` error occurs when the print function in Python attempts to print a character that cannot be encoded in the current character set. This error often happens when dealing with non-ASCII characters, such as those in foreign languages or special symbols.


## Understanding the Error

When Python tries to print a character, it needs to convert it to a string format that can be displayed in the console or terminal. This process involves encoding the character in the character set used by the system.

The "charmap" codec is a codec used to handle character encoding in Windows systems. When trying to encode a character that is not recognized by the system's character set, Python can't encode the character, and hence the error is raised.

The error message provides information on the exact character that is causing the problem, and how it maps to an undefined value.


## Solutions

### Use a Different Encoding

One solution is to use a different character encoding that supports the problematic character. For example, using the "utf-8" encoding instead of the default "charmap" encoding can handle a wider range of characters:

``` python
import sys
print("Hello ελληνικά".encode(sys.stdout.encoding, errors='replace'))
```

In this code, we specify the encoding to be the one used by the console or terminal, which is `sys.stdout.encoding`. The `errors='replace'` parameter tells Python to replace any problematic characters with a question mark, instead of raising an error.


### Use the 'io' module

Another solution is to use the `io` module to open the console or terminal in a different character encoding:

``` python
import io, sys
sys.stdout = io.TextIOWrapper(sys.stdout.detach(), encoding='utf-8')
```

This code sets the standard output stream `sys.stdout` to use the "utf-8" encoding, allowing it to handle a larger range of characters.


### Use 'unicode_escape' for Printing

A third solution is to use the "unicode_escape" encoding to print a Unicode string as a series of escape sequences:

``` python
print("Hello \u03b5\u03bb\u03bb\u03b7\u03bd\u03b9\u03ba\u03ac".encode('unicode_escape').decode())
```

In this code, we first encode the string using the "unicode_escape" encoding, which replaces non-ASCII characters with escape sequences. Then we decode the resulting byte string into a Unicode string that can be printed.


## Conclusion

The `UnicodeEncodeError: 'charmap' codec can't encode` error is a common issue when working with non-ASCII characters in Python. By using a different encoding, opening the console or terminal with a different encoding, or printing as escape sequences, you can overcome this error and display non-ASCII characters correctly.
