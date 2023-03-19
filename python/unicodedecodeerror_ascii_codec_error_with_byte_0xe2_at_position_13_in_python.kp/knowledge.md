---
title: There is an error in decoding unicode which says that the 'ascii' codec is unable to decode the byte sequence starting from position 13 as the ordinal value is not within the range of 128
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: This error occurs when trying to read or decode a string with non-ASCII characters using the ASCII codec.
---

**Contents**

[TOC]

Section 1: Explanation of the Error Message

The error message "UnicodeDecodeError: 'ascii' codec can't decode byte 0xe2 in position 13: ordinal not in range(128)" in Python is raised when the Python interpreter encounters a character that cannot be decoded to ASCII. This error typically occurs when a program tries to decode text on a system where the default encoding is not UTF-8.

Section 2: Causes of the Error Message

The most common cause of this error is when the encoded text contains characters that are not ASCII characters, but the program is trying to decode the text as ASCII. Typically, this happens when text is read from a file or another source that uses a different encoding scheme than the one the program is expecting.

Another common cause of this error is when the program is running in an environment where the default encoding is ASCII, which is not capable of representing non-ASCII characters.

Section 3: How to Fix the Error Message

There are several ways to fix this error message, depending on the cause of the problem:

1. Specify the encoding: The simplest solution is to specify the correct encoding when reading or decoding text. For example, if the incoming text is encoded in UTF-8, the program should specify UTF-8 when reading the text.

2. Change the default encoding: It's also possible to change the default encoding of the Python interpreter by setting the PYTHONIOENCODING environment variable. This approach is not recommended, as it can lead to unexpected behavior in other parts of the program.

3. Use Unicode strings: Another approach is to use Unicode strings in the program, which can represent all characters in any encoding. This approach requires modifying the program to use Unicode strings throughout.

Section 4: Conclusion

The "UnicodeDecodeError" in Python indicates that the program is trying to decode text as ASCII that contains non-ASCII characters. This error can be fixed by setting the correct encoding, changing the default encoding, or using Unicode strings in the program. It's important to ensure that text is always read and decoded with the correct encoding to avoid this error.
