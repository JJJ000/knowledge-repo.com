---
title: Can you explain the contrast between isinstance('aaa', basestring) and isinstance('aaa', str)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: isinstance(`aaa`, basestring) is equivalent to isinstance(`aaa`, str) in Python 3.x as basestring is removed from the language, but in Python 2.x, isinstance(`aaa`, basestring) also checks if the object is an instance of unicode.
---

**Contents**

[TOC]

Section 1: The Basics of isinstance() Function
---

Before discussing the difference between `isinstance('aaa', basestring)` and `isinstance('aaa', str)` in Python, it is essential to understand the basics of the `isinstance()` function.

In Python, `isinstance()` is a built-in function that returns `True` if the specified object is an instance of the specified class, and `False` otherwise. It takes two arguments: the object to check and the class or tuple of classes to check against.

Here is the syntax for the `isinstance()` function:

```
isinstance(object, classinfo)
```

- `object`: The object to check.
- `classinfo`: A class, type, or tuple of classes and types.

Section 2: Understanding basestring and str Classes
---

In Python 2.x, there are two string classes: `basestring` and `str`. However, in Python 3.x, the `basestring` class has been removed, and there is only one string class, `str`.

- `basestring`: It is the superclass of `str` and `unicode` classes in Python 2.x. It is an abstract type, meaning you can't create instances of it. Its purpose is to enable checking if an object is an instance of a `str` or `unicode` type.
- `str`: It is a built-in string class that represents a sequence of Unicode characters in Python. It is used to handle Unicode strings.

Section 3: The Difference between isinstance('aaa', basestring) and isinstance('aaa', str)
---

The `isinstance('aaa', basestring)` function returns `True` in both Python 2.x and Python 3.x because the `basestring` class is the superclass of the `str` class. So, any string object is an instance of `basestring`.

On the other hand, the `isinstance('aaa', str)` function only returns `True` in Python 3.x because there is no `basestring` class in Python 3.x. In Python 3.x, all strings are Unicode strings, and they are represented by the `str` class. However, in Python 2.x, if `isinstance('aaa', str)` is used, it will only return `True` if the object is an instance of the `str` class, but not if it is an instance of the `unicode` class.

In general, it is recommended to use `isinstance(obj, str)` to check if an object is a string in both Python 2.x and Python 3.x.

Section 4: Conclusion
---

In conclusion, the difference between `isinstance('aaa', basestring)` and `isinstance('aaa', str)` in Python lies in the fact that the `basestring` class is only available in Python 2.x, while in Python 3.x, there is only one string class, `str`. Therefore, for checking if an object is a string in both Python 2.x and Python 3.x, it is recommended to use `isinstance(obj, str)`.
