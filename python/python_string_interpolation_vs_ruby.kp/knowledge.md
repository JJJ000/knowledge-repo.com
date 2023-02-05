---
title: What is the Python equivalent to ruby's string interpolation?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, Python has a similar feature called f-strings which allows for string interpolation.
---

**Contents**

[TOC]

**Yes**

**Python Format Strings**

Python supports formatting values into strings. Although this can include very complicated expressions, the most basic usage is to insert values into a string with the %s placeholder.

```
name = "John"
print("Hello, %s!" % name)
```

**Python f-Strings**

Python 3.6+ introduced the new f-string syntax, which is similar to Ruby's string interpolation. This allows you to embed variables directly into strings, using the same syntax as Ruby.

```
name = "John"
print(f"Hello, {name}!")
```

**Conclusion**

Python has two methods for string interpolation: format strings and f-strings. Both of these methods are similar to Ruby's string interpolation, and can be used to embed variables into strings.
