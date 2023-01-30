---
title: Changing a string to a boolean value in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: In Python, you can convert a string to a boolean using the bool() function.
---

**Contents**

[TOC]

# String to Boolean

## String Representation of Boolean
In Python, a string representing a boolean can take the values of "True" or "False". These strings can be converted to boolean values using the `bool()` function.

## Conversion using `bool()`
When using `bool()`, if the string is "True" it will return `True`, and if the string is "False" it will return `False`. All other strings will return `False`.

## Example

```python
string_1 = "True"
string_2 = "False"

bool_1 = bool(string_1)
bool_2 = bool(string_2)

print(bool_1) # prints True
print(bool_2) # prints False
```

## Other Conversion Methods
In addition to the `bool()` function, the `ast.literal_eval()` function can also be used to convert a string representation of a boolean to a boolean value. This method can be used to convert strings of other data types, such as integers or floats, as well.
