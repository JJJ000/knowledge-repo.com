---
title: What is the method to verify if a Python string is in ascii format?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Check if all the characters in the string have an ASCII code between 0 and 127.
---

**Contents**

[TOC]

## Introduction
Python provides several methods to check if a string is ASCII or not. ASCII stands for American Standard Code for Information Interchange. It is a character encoding standard for electronic communication. ASCII encodes 128 specified characters into seven-bit integers. In this tutorial, we will discuss some methods to check if a string is in ASCII.

## Using 'ascii' encoding
One way to check if a string is in ASCII is by encoding the string with the 'ascii' encoding. The 'ascii' encoding only encodes ASCII characters. So, if the encoding succeeds, it means that the string is in ASCII. If the encoding fails, it means the string contains non-ASCII characters.

```python
def is_ascii(string):
    try:
        string.encode('ascii')
        return True
    except UnicodeEncodeError:
        return False

# example usage
print(is_ascii('Hello, world!')) # True
print(is_ascii('안녕하세요')) # False
```

## Using 'string.printable'
Another way to check if a string is in ASCII is by checking if all the characters in the string are 'printable'. The 'string' module in Python provides a constant called 'printable' which contains all the printable ASCII characters. 

```python
import string

def is_ascii(string):
    for char in string:
        if char not in string.printable:
            return False
    return True

# example usage
print(is_ascii('Hello, world!')) # True
print(is_ascii('안녕하세요')) # False
```

## Using regex
We can use regular expressions to check if a string is in ASCII or not. The regular expression [^\x00-\x7F] matches any character that is not in the range of ASCII characters. We can use this regular expression to check if a string is in ASCII or not.

```python
import re

def is_ascii(string):
    return not bool(re.search('[^\x00-\x7F]', string))

# example usage
print(is_ascii('Hello, world!')) # True
print(is_ascii('안녕하세요')) # False
```

## Conclusion
In this tutorial, we discussed some methods to check if a string is in ASCII. We can use the 'ascii' encoding, the 'string.printable' constant, or regular expressions to check if a string is in ASCII.
