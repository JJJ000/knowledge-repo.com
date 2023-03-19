---
title: An alternative method for declaring several variables simultaneously with a greater sense of sophistication
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using tuple unpacking, we can declare multiple variables at the same time in Python.
---

**Contents**

[TOC]

## Use Tuple Unpacking

One way to declare and initialize multiple variables at the same time in Python is to use tuple unpacking. Basically, you assign a tuple of values to a tuple of variables, and Python will automatically unpack the values and assign them to the variables. Here's an example:

```python
x, y, z = 1, 2, 3
```

This is equivalent to writing:

```python
x = 1
y = 2
z = 3
```

## Use List Unpacking

You can also use list unpacking in a similar way, but with square brackets instead of parentheses:

```python
[x, y, z] = [1, 2, 3]
```

This is equivalent to the tuple unpacking example above.

## Use Multiple Assignments

Another option is to use multiple assignments, which works best when initializing variables with the same value:

```python
x = y = z = 0
```

This assigns the value 0 to all three variables.

## Use Dictionary Unpacking

In Python 3.7 and above, you can also use dictionary unpacking to assign values to multiple variables at once. This requires you to create a dictionary with keys that match the variable names and values that correspond to the initial values:

```python
values = {'x': 1, 'y': 2, 'z': 3}
x, y, z = values.values()
```

This assigns the values 1, 2, and 3 to variables x, y, and z respectively.
