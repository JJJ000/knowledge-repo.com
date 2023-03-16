---
title: What is an alternative way to check the existence of an integer value in a Python enum apart from using try/catch statements during testing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the `value in Enum` syntax to check if an int value exists in Python Enum (e.g. `my\_value in MyEnum`).
---

**Contents**

[TOC]

Section 1: Introduction to Python Enum

Python Enum is a built-in data type that allows us to define a set of constant values with associated names. By using Enums, we can define a set of values that are related to each other and share a common purpose.

Section 2: Checking if an int value exists in an Enum

In order to check if an integer value exists in a Python Enum, we can use the `__members__` attribute of the Enum class. This attribute returns a dictionary of the members of the Enum, where the key is the member name and the value is the member object.

For example, if we have the following Enum:

```
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3
```

We can check if the value `2` is a member of the Enum by using the `__members__` attribute as follows:

```
2 in Color.__members__.values()
```

This will return `True` if the value is a member of the Enum, and `False` otherwise.

Section 3: Using a helper function for readability

To make the code cleaner and easier to read, we can create a helper function that encapsulates the above logic:

```
def is_member(val, enum):
    return val in enum.__members__.values()
```

Then we can use this function to check if a value exists in an Enum:

```
is_member(2, Color)  # Returns True
```

Section 4: Conclusion

We can check if an int value exists in a Python Enum by using the `__members__` attribute, which returns a dictionary of the Enum members. By creating a helper function, we can make the code more readable and easier to use.
