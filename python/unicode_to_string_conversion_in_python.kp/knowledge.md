---
title: Transform a unicode sequence into a string with special characters in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the .encode() method to convert a Unicode string to a string containing extra symbols.
---

**Contents**

[TOC]

### String Conversion
Python provides a built-in `unicode()` function that can convert a Unicode string to a string.

### Syntax
The syntax for `unicode()` is:

```
unicode(string, encoding)
```

### Example
The following example shows how to convert a Unicode string to a string containing extra symbols:

```
# Unicode string
unicode_string = u'\u00A9 Copyright 2020'

# Convert to string
string = unicode(unicode_string, 'utf-8')

# Print string
print(string)

# Output: © Copyright 2020
```

### Conclusion
The `unicode()` function can be used to convert a Unicode string to a string containing extra symbols.
