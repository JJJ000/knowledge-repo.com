---
title: Comprehending the repr() method functionality in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The repr( ) function in Python returns a printable representation of an object.
---

**Contents**

[TOC]

Section 1: Definition and Purpose of repr( )

The `repr()` function in Python is a built-in function that returns a string representation of an object. The `repr()` function provides more information about an object as compared to the `str()` function. The returned string from the `repr()` function can be used to re-create the object. The `repr()` function is especially useful in debugging and testing. The `repr()` function is also commonly used for displaying the output of user-defined classes.

Section 2: Syntax of repr( )

The syntax of the `repr()` function is straightforward. It only takes one argument- the object you want to represent as a string. The syntax is as follows:

```
repr(object)
```

Where `object` is the object that you want to represent as a string.

Section 3: Differences between repr( ) and str( )

The `repr()` and `str()` functions are similar in that they both return a string representation of an object. However, the `str()` function returns a printable string, while the `repr()` function returns an unambiguous string representation of an object. The `repr()` function aims to return a string that can be used to recreate the original object. The string returned by `repr()` can be passed as an argument to the `eval()` function to recreate the original object.

Section 4: Example usage of repr( )

Here is an example of using the `repr()` function:

```
class Fruit:
    def __init__(self, name, color):
        self.name = name
        self.color = color

    def __repr__(self):
        return f"{self.__class__.__name__}({self.name!r}, {self.color!r})"

fruit = Fruit("Apple", "Red")
print(repr(fruit))
```

Output:
```
Fruit('Apple', 'Red')
```
In this example, we have defined a `Fruit` class and defined the `__repr__()` method. The `__repr__()` method here returns a string that represents the `Fruit` object in a format that can be used to create a new instance of this object. The `repr()` function is used to return this string representation that we can now use in debugging, testing or displaying the `fruit` object.
