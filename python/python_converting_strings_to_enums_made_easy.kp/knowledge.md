---
title: How to change a string into an enum in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the Enum function from the enum module in Python to convert a string into an Enum.
---

**Contents**

[TOC]

## Introduction
In Python, an `enum` is a special type that allows for a set of predefined named values. This makes it easy to define a specific set of options that can be used in a program. Converting a string to an `enum` allows for the comparison of the string value against the named values of the `enum`. In this article, we will discuss how to convert a string to an `enum` in Python.

## Defining an Enum
To define an `enum` in Python, we first need to import the `enum` module. The `enum` module provides a class called `Enum` which we can use to create our enumeration. We define our enumeration as follows:

```python
from enum import Enum

class MyEnum(Enum):
    FIRST_VALUE = 1
    SECOND_VALUE = 2
    THIRD_VALUE = 3
```

Now we have defined an `enum` named `MyEnum` with three named values: `FIRST_VALUE`, `SECOND_VALUE`, and `THIRD_VALUE`. Each named value is associated with an integer value.

## Converting a String to an Enum
To convert a string to an `enum` in Python, we can use the `Enum` class's `__members__` attribute. The `__members__` attribute provides a dictionary of the named values of the `enum`. We can use this dictionary to check if the given string matches any of the named values. If a match is found, we can return the corresponding named value. Here is an example:

```python
from enum import Enum

class MyEnum(Enum):
    FIRST_VALUE = 1
    SECOND_VALUE = 2
    THIRD_VALUE = 3

def string_to_enum(str_value):
    for name, member in MyEnum.__members__.items():
        if name == str_value:
            return member
    return None
```

In this example, we define a function named `string_to_enum` that takes a string argument named `str_value`. The function iterates over the named values of the `MyEnum` `enum` and checks if any of them match the `str_value`. If a match is found, the corresponding named value is returned. If no match is found, `None` is returned.

## Using the String to Enum Conversion
Now that we have defined our `enum` and created a function to convert a string to an `enum`, we can use our conversion as follows:

```python
my_value = "SECOND_VALUE"
value_enum = string_to_enum(my_value)

if value_enum == MyEnum.SECOND_VALUE:
    print("Value is Second Value")
else:
    print("Unknown Value")
```

In this example, we first define a string named `my_value`. We then pass this string to our `string_to_enum` function to get the corresponding `enum` value. We then check if the `enum` value is equal to `MyEnum.SECOND_VALUE`. If it is, we print "Value is Second Value". If not, we print "Unknown Value".

## Conclusion
Converting a string to an `enum` in Python can be useful in many situations. It allows for easy comparison of a string value against a set of named values. By defining an `enum` and using the `Enum` class's `__members__` attribute, we can easily convert a given string to its corresponding `enum` value.
