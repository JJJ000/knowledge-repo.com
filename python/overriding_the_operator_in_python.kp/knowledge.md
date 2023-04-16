---
title: What is the process for overriding the [] operator in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can override the [] operator by defining a \_\_getitem\_\_() method in the class.
---

**Contents**

[TOC]

# Section 1: Overview

The [] operator, also known as the subscription operator, is used to access elements of a sequence or a mapping. In Python, this operator can be overridden by defining it as a method within a custom class.

# Section 2: Defining the Operator

To override the [] operator, define a method within the desired class with the name `__getitem__`. This method should take two arguments, `self` and `key`, and should return the desired value.

# Section 3: Example

The following example shows how to override the [] operator in a custom class.

```python
class MyClass:
    def __getitem__(self, key):
        return "The value for key {} is 42".format(key)

my_object = MyClass()
print(my_object[5]) # prints "The value for key 5 is 42"
```

# Section 4: Further Reading

For more information on overriding the [] operator, see the official Python documentation: https://docs.python.org/3/reference/datamodel.html#object.__getitem__
