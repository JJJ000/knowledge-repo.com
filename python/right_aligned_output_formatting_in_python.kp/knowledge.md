---
title: Align the output string to the right while formatting it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: String formatting can be right aligned in Python using the `>` character in the formatting specifier.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, we can format an output string using the .format() method. This method provides several options for left, center or right alignment of the output. In this article, we will focus on right alignment and explore the various ways in which we can achieve it.

Section 2: Using the format() method for right alignment
The format() method provides the '>' character for right alignment. We can place this character immediately after the variable name or string that we want to right-align.

Example:
```python
name = "John"
age = 24
output = "{:>10}: {:>5}".format(name, age)
print(output)
```
Output:
```
      John:    24
```
In the above example, the '>' character is used to right-align the name and age variables.

Section 3: Using the rjust() function for right alignment
Another way to right-align a string is by using the rjust() function. This function takes an argument that specifies the width of the output string and an optional argument that specifies the fill character. By default, the fill character is a space.

Example:
```python
name = "John"
age = 24
output = name.rjust(10) + ": " + str(age).rjust(5)
print(output)
```
Output:
```
      John:    24
```
In the above example, we first right-align the name and age using the rjust() function and then concatenate the two strings.

Section 4: Conclusion
In this article, we explored two ways to right-align an output string in Python. We learned that we can use the '>' character with the .format() method or use the rjust() function to achieve right alignment. We hope this article helps you in your Python programming journey.
