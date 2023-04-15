---
title: What is the method of presenting a floating-point number with two decimal places?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `{.2f}` format specifier in the print statement to display a float with two decimal places in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, a float is a data type that represents decimal numbers. By default, Python displays floats with several decimal places. However, in some cases, it may be necessary to display a float with two decimal places for better reading or formatting purposes. In this guide, we will discuss different ways to display a float with two decimal places in Python.

Section 2: Using String Formatting
Python's string formatting feature allows us to format a string in a particular way. We can use the formatting feature to display a float with two decimal places. Here is an example of how to use string formatting to display a float with two decimal places:

```python
x = 2.345
print("The value of x is {:.2f}".format(x))
```
Output: `The value of x is 2.35`

In the above example, we used the {:.2f} format specifier to display x with two decimal places. The f stands for float, and the 2 stands for the number of decimal places.

Section 3: Using the round() Function
Python's built-in round() function is another way to display a float with two decimal places. Here is an example:

```python
x = 2.345
rounded_x = round(x, 2)
print("The value of x is", rounded_x)
```
Output: `The value of x is 2.35`

In the above example, we used the round() function to round x to two decimal places. The second argument to the round() function is the number of decimal places we want to round to.

Section 4: Conclusion
In this guide, we discussed different ways to display a float with two decimal places in Python. By using string formatting and the round() function, we can easily format floats for better readability and formatting purposes.
