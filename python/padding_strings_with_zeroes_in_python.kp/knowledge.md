---
title: What is the best way to add zeroes to the end of a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the str.zfill() method to pad a string with zeroes.
---

**Contents**

[TOC]

## Using rjust()
The `rjust()` method can be used to pad a string with zeroes in Python.

### Syntax
```python
string.rjust(width[, fillchar])
```

### Parameters
- **width** - This is the total width of the string.
- **fillchar** - This is the character to pad the string with (default is a space).

### Example
```python
# Print the string padded with zeroes
print('123'.rjust(8, '0'))
```

### Output
```
00000123
```
