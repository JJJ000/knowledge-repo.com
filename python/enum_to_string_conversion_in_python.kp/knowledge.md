---
title: How to convert a string into an enum's value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can get the value of an enum on string conversion in Python by accessing its value attribute.
---

**Contents**

[TOC]

Section 1: Enum basics
Enums are a type of data structure in Python that allow you to define a set of named constants. These constants can be used to represent different values for a particular variable or property. Enums are useful for creating more readable and maintainable code.

Here's an example of an enum definition in Python:

```
from enum import Enum

class Color(Enum):
  RED = 1
  GREEN = 2
  BLUE = 3
```

In this example, `Color` is an enum class that defines three constants: `RED`, `GREEN`, and `BLUE`. Each constant has an associated integer value.

Section 2: String conversion of enums
Enums can be converted to strings using the `str()` or `repr()` built-in functions. By default, these functions return the name of the enum constant. For example:

```
color = Color.RED
print(str(color))  # prints "Color.RED"
print(repr(color)) # prints "<Color.RED: 1>"
```

In addition to the default behavior, you can provide a custom implementation of the `__str__()` or `__repr__()` methods to control how enums are converted to strings.

Section 3: Getting the value of an enum
To get the integer value associated with an enum constant, you can use the `.value` property. For example:

```
color = Color.RED
print(color.value) # prints 1
```

This property returns the integer value associated with the constant.

Section 4: Combining string conversion and getting the enum value
To get the integer value of an enum constant using a string representation of the constant, you can use the `getattr()` built-in function. This function returns the attribute value of an object given its name as a string.

For example:

```
color_str = 'Color.RED'
color = getattr(Color, color_str)
print(color.value) # prints 1
```

In this example, we use `getattr()` to get the `Color.RED` constant from the `Color` enum class. We then access the `.value` property of the constant to get its integer value.
