---
title: The Python string is printed as [u'string']
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The `u` prefix indicates that the string is a Unicode string.
---

**Contents**

[TOC]

Introduction to Python String Printing
--------------------------------------

In Python, strings are sequence of characters. To print a string, we can use the print() function. When we print a string in Python, it may show up with a prefix "[u'"] before the actual string value. Let's explore why this happens and how we can remove it.


Unicode Strings in Python
--------------------------

The prefix "[u'"] before a string in Python indicates that the string is a Unicode string. Python 2 had two types of strings: ASCII strings and Unicode strings. ASCII strings could only represent seven bits of data, while Unicode strings could represent 16 bits. To create a Unicode string in Python 2, we would need to add a "u" prefix before the quotes. However, in Python 3, all strings are Unicode by default. So, when we see a string with a prefix "[u']", it's because we are using Python 2.


Converting Python 2 Strings to Python 3 Strings
-------------------------------------------------

If we want to remove the "[u']" prefix from strings in Python 2, we can encode the string using UTF-8 encoding. This will convert the string to a Python 3 compatible string, which will not have a prefix. For example:
```
st = u"Hello"
st = st.encode('utf-8')
print(st)
```
This will output "b'Hello'", which is a Python 3 compatible string. However, if we want to stick to Python 2, we can simply ignore the prefix.


Conclusion
-----------

The prefix "[u']" before a string in Python indicates that it is a Unicode string. If we are using Python 2 and want to remove this prefix, we can encode the string using UTF-8 encoding. However, if we are using Python 3, all strings are Unicode by default and the prefix should not appear.
