---
title: Change an integer to a string in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: str() can be used to convert an integer to a string in Python.
---

**Contents**

[TOC]

## Using str()
The `str()` function is the most common way to convert an integer to a string in Python.

Example:
```
x = 5

x_str = str(x)

print(x_str)
```
Output:
```
'5'
```

## Using format()
The `format()` method is another way to convert an integer to a string in Python.

Example:
```
x = 5

x_str = format(x)

print(x_str)
```
Output:
```
'5'
```

## Using repr()
The `repr()` function can also be used to convert an integer to a string.

Example: 
```
x = 5

x_str = repr(x)

print(x_str)
```
Output:
```
'5'
```

## Using f-strings
The `f-strings` method is a more modern way to convert an integer to a string in Python.

Example:
```
x = 5

x_str = f'{x}'

print(x_str)
```
Output:
```
'5'
```
