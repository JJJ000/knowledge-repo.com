---
title: Differences between python's __str__ and __unicode__ methods
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: In Python 3, there is no difference between \_\_str\_\_ and \_\_unicode\_\_, as both are replaced by \_\_str\_\_.
---

**Contents**

[TOC]

Section 1: Introduction
Python is a programming language that supports both ASCII and Unicode characters. In Python, strings are sequences of characters that can be represented using either the str or the unicode data types. The str and unicode data types are used to represent strings of ASCII and Unicode characters respectively.

Section 2: The str Function
The str function is used to convert a string or any other object into a string representation. It returns an ASCII string representation of the input object. The str function is useful when we want to print strings, concatenate strings, or use strings as keys in dictionaries. In Python 3, the default string type is the str data type.

Section 3: The unicode Function
The unicode function is used to convert a string or any other object into a Unicode string representation. It returns a Unicode representation of the input object. The unicode function is useful when we want to work with strings that contain non-ASCII characters. In Python 2, the default string type is the str data type, which only supports ASCII characters. However, Python 2 also has a separate unicode data type that can be used to represent strings with non-ASCII characters.

Section 4: The __str__ and __unicode__ Methods
Python classes can define the __str__ and __unicode__ methods to specify how objects of the class should be converted to strings. The __str__ method is used to define the ASCII representation of an object, while the __unicode__ method is used to define the Unicode representation of an object. In Python 3, the __unicode__ method is not used, and the __str__ method should return a string with Unicode characters. In Python 2, the __str__ method should return an ASCII string, while the __unicode__ method should return a Unicode string. The appropriate method to use depends on the Python version being used and the type of string representation needed. 

Conclusion:
In conclusion, the str and unicode functions are used to convert objects into ASCII and Unicode string representations respectively. The choice of whether to use str or unicode depends on whether the string contains non-ASCII characters or not. The __str__ and __unicode__ methods can be used to define how objects should be converted to strings. The appropriate method to use depends on the Python version being used and the type of string representation needed.
