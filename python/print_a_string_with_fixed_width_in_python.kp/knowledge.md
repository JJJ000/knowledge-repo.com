---
title: What is the method for printing a string with a predetermined width?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the formatting syntax {<width} within the print statement to left-align the string to a fixed width.
---

**Contents**

[TOC]

## Introduction
Printing a string at a fixed width in Python is a useful task for formatting output according to specific requirements. This can be achieved using the `str.format()` method, which is used to format strings in Python. In this tutorial, we will explain how to print a string at a fixed width in Python using different methods.

## Method 1: Using the str.ljust() and str.rjust() methods
The `str.ljust()` and `str.rjust()` methods can be used to print a string at a fixed width. These methods align the string to the left or right and fill the remaining space with a specified character.

### Syntax
```python
string.ljust(width, fillchar)
string.rjust(width, fillchar)
```

### Example
```python
text = 'Hello'
width = 10
fillchar = '*'
left_aligned_text = text.ljust(width, fillchar)
right_aligned_text = text.rjust(width, fillchar)
print(left_aligned_text)  # Output: 'Hello*****'
print(right_aligned_text)  # Output: '*****Hello'
```

## Method 2: Using the format() method with the {:<} and {:>} placeholders
The `format()` method can be used with the `:<` and `:>` characters to align the string to the left or right, respectively. The width of the field can also be specified using a numerical value inside the curly braces.

### Syntax
```python
'{:<width}'.format(string)
'{:>width}'.format(string)
```

### Example
```python
text = 'Hello'
width = 10
left_aligned_text = '{:<{width}}'.format(text, width=width)
right_aligned_text = '{:>{width}}'.format(text, width=width)
print(left_aligned_text)  # Output: 'Hello     '
print(right_aligned_text)  # Output: '     Hello'
```

## Conclusion
Printing a string at a fixed width in Python can be achieved using different methods. The `str.ljust()` and `str.rjust()` methods can be used to align the string to the left or right and fill the remaining space with a specified character. The `format()` method with the `:<` and `:>` characters and a numerical value inside the curly braces can also be used to align the string to the left or right and specify the width of the field.
