---
title: Obtain the name of the enumeration based on its value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can use a dictionary or the Enum class`s \_\_members\_\_ attribute to map the enum values to their names.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, Enumerations (or enums) are a set of predefined values that represent a finite set of options. Enums are structured as classes, where each value is an instance of the class. Enums can be useful for representing states, settings, or options that should only take on certain values. In this guide, we'll explore how to get the name of an enumeration by its value in Python.

Section 2: Example Enum
To demonstrate how to get the name of an enumeration by its value, let's define an example enum, which represents the days of the week:

```
from enum import Enum

class Weekday(Enum):
    MONDAY = 1
    TUESDAY = 2
    WEDNESDAY = 3
    THURSDAY = 4
    FRIDAY = 5
    SATURDAY = 6
    SUNDAY = 7
```

Section 3: Getting the Name of an Enumeration by Value
To get the name of an enumeration by its value, we can use the `name` attribute of the enum member. Here's an example:

```
value = Weekday.MONDAY
name = value.name
print(name) # Output: 'MONDAY'
```
In this example, we get the `MONDAY` value of the `Weekday` enumeration and then use the `name` attribute to get the name of the value.

If we have the value as an integer, we can use the `Weekday(value)` syntax to get the corresponding enumeration member, and then use the `name` attribute to get its name:

```
value = 1
weekday = Weekday(value)
name = weekday.name
print(name) # Output: 'MONDAY'
```

Section 4: Conclusion
In Python, we can easily get the name of an enumeration value by using the `name` attribute of the corresponding enum member. By using enums, we can better organize and structure our code and make it more readable and maintainable.
