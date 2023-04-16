---
title: Translate a hexadecimal string into an integer in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the int() function with a base of 16 to convert a hex string to an integer in Python.
---

**Contents**

[TOC]

# Section 1: Overview

Converting a hexadecimal string to an integer in Python is a relatively straightforward process. By using the built-in int() function with a base of 16, you can easily convert a hexadecimal string to an integer.

# Section 2: Syntax

The syntax for converting a hexadecimal string to an integer in Python is as follows:

```
int(hex_string, 16)
```

# Section 3: Example

For example, to convert the hex string "0xA4" to an integer, you would use the following code:

```
int("0xA4", 16)
```

# Section 4: Output

This will return the result of 164.
