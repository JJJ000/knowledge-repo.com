---
title: What is the method to display unicode characters in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the \u followed by the four-digit hexadecimal representation of the Unicode character in a single- or double-quoted string.
---

**Contents**

[TOC]

Introduction:

Python provides great support for Unicode characters. Unicode is a universal character encoding standard, which defines a unique number for each character. Python has built-in support for Unicode in the form of Unicode strings. In this tutorial, we will discuss different ways of printing Unicode characters in Python.

1. Using the character's Unicode Code Point:

One way to print Unicode characters in Python is to use their Unicode code point. The Unicode code point is a unique number assigned to each character in the Unicode standard. We can use the "\u" escape sequence followed by the character's code point to print it.

For example, to print the Unicode character "©", which has a code point of U+00A9, we can use the following code:

```
print('\u00A9')
```

Output:

```
©
```

2. Using Unicode strings:

Another way to print Unicode characters in Python is to use Unicode strings. A Unicode string is a sequence of Unicode characters enclosed in quotes. We can create a Unicode string by prefixing the string literal with a "u" character.

For example, to print the Unicode character "©", we can create a Unicode string as follows:

```
print(u'\u00A9')
```

Output:

```
©
```

3. Using the "ord" and "chr" functions:

We can also use the "ord" and "chr" functions to print Unicode characters in Python. The "ord" function returns the Unicode code point of a character, whereas the "chr" function returns the character for a given Unicode code point.

For example, we can print the Unicode character "©" as follows:

```
print(chr(0xA9))
```

Output:

```
©
```

4. Using the "encode" and "decode" methods:

We can also use the "encode" and "decode" methods to print Unicode characters in Python. The "encode" method converts a Unicode string to a byte sequence, whereas the "decode" method converts a byte sequence to a Unicode string.

For example, we can print the Unicode character "©" as follows:

```
print('\xA9'.decode('utf-8'))
```

Output:

```
©
```

Conclusion:

In this tutorial, we discussed different ways of printing Unicode characters in Python. We can use the character's Unicode code point, Unicode strings, the "ord" and "chr" functions, and the "encode" and "decode" methods to print Unicode characters.
