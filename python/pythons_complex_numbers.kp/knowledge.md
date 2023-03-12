---
title: The topic of python's complex numbers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python supports complex numbers using the notation `a + bj` or `a + bi`, where `j` or `i` represents the imaginary unit.
---

**Contents**

[TOC]

# What are Complex Numbers?

Complex numbers are mathematical numbers that express real and imaginary numbers. A complex number is represented in the form of a+ib, where a and b are real numbers, and i is the imaginary unit. 

For example, (3+4i) is a complex number where a=3, b=4, and i is the imaginary unit.

Python provides complex numbers as a built-in data type that can be used to perform various mathematical operations.

# Creating Complex Numbers in Python

To create a complex number in Python, we can use the `complex()` function or directly assign values to variables. Here are a few examples:

```python
# using the complex() function
comp_num_1 = complex(3, 4) # 3+4i
comp_num_2 = complex(0, 2) # 2i

# directly assigning values
comp_num_3 = 2+3j
comp_num_4 = -1-2j
```

# Operations with Complex Numbers

Python provides various mathematical operations that can be performed with complex numbers. These include addition, subtraction, multiplication, division, and more.

```python
# addition
result = comp_num_1 + comp_num_2 # 3+6i

# subtraction
result = comp_num_3 - comp_num_4 # 3+5j

# multiplication
result = comp_num_1 * comp_num_3 # -6+17j

# division
result = comp_num_1 / comp_num_4 # -0.2-0.6j

# absolute value
abs_value = abs(comp_num_3) # 3.605551275463989
```

# Conclusion 

In conclusion, complex numbers are a vital part of mathematics and can be easily used in Python for mathematical operations. Python's built-in complex number data type provides several functions that can be used to perform various complex number operations, including addition, subtraction, multiplication, division, and more.
