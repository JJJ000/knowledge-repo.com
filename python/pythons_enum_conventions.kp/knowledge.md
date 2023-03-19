---
title: What is the standard approach to using enums in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The common practice for enums in Python is to use the Enum class from the built-in enum module.
---

**Contents**

[TOC]

Python does not have a built-in Enum type, but there are different ways to implement enums in Python code. Here are a few common practices:

## Using Enum from the enum package

The `enum` package is part of the Python standard library since version 3.4. It provides a comprehensive implementation of enumeration types.

```python
from enum import Enum

class Color(Enum):
    RED = 1
    GREEN = 2
    BLUE = 3
```

In this example, we define an enumeration type `Color` with three possible values `RED`, `GREEN`, and `BLUE`. Each value is associated with an integer value; by default, the integer values are assigned to the names in the order they are defined.

We can use the enumeration values in Python code like this:

```python
>>> Color.RED
<Color.RED: 1>
>>> Color.GREEN.value
2
>>> Color.BLUE.name
'BLUE'
```

We can also iterate over the values of an enum:

```python
for color in Color:
    print(color)
```

This will output:

```
Color.RED
Color.GREEN
Color.BLUE
```

Using `Enum` provides a robust and flexible way to implement enums in Python code, but it requires importing an external package.

## Using constants with descriptive names

Another way to define enums in Python is to use constants with descriptive names. For example:

```python
RED = 'red'
GREEN = 'green'
BLUE = 'blue'
```

Here, we define three constants for the three possible values of a `Color` enum. The names of the constants are self-descriptive, and we can use them in Python code like this:

```python
color = RED
if color == GREEN:
    print('green')
elif color == BLUE:
    print('blue')
else:
    print('red')
```

This approach is simple and does not require any additional package, but it puts the burden of maintaining the list of allowed values on the developer.

## Using namedtuple

Another way to create an enum-like structure in Python is to use the `namedtuple` from the `collections` package:

```python
from collections import namedtuple

Color = namedtuple('Color', 'RED GREEN BLUE')
```

In this example, we define a new `namedtuple` type `Color` with three fields `RED`, `GREEN`, and `BLUE`. We can use the values of the `Color` tuple like this:

```python
color = Color.RED
if color == Color.GREEN:
    print('green')
elif color == Color.BLUE:
    print('blue')
else:
    print('red')
```

Using `namedtuple` can be an elegant way to define enums in Python, but it has some limitations, such as the lack of support for iteration, auto-numbering, and name collision protection.
