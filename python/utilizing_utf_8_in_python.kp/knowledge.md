---
title: Manipulating utf-8 encoding in Python code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To work with UTF-8 encoding in Python source, use the `utf-8` encoding declaration at the top of the source file.
---

**Contents**

[TOC]

# Section 1: Setting the Encoding

The default encoding for Python source files is UTF-8. To ensure that this is the case, the first line of the Python source file should contain the following:

```
# -*- coding: utf-8 -*-
```

This line should be placed at the top of the file, before any other code.

# Section 2: Working with Strings

When working with strings, it is important to use the correct encoding. To do this, strings should be marked as UTF-8 by prefixing them with the letter 'u'. For example:

```
my_string = u'This is a UTF-8 string.'
```

# Section 3: Printing Strings

When printing strings, it is important to ensure that the correct encoding is used. To do this, the 'encode' method should be used. For example:

```
print my_string.encode('utf-8')
```

# Section 4: Working with Files

When working with files, it is important to ensure that the correct encoding is used. To do this, the 'open' method should be used with the encoding parameter set to 'utf-8'. For example:

```
my_file = open('my_file.txt', 'w', encoding='utf-8')
```
