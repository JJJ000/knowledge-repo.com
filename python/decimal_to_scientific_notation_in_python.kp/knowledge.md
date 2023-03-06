---
title: Represent a decimal number in scientific notation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the string formatting method `{.2e}`.format(number) to display a decimal in scientific notation with two decimal places.
---

**Contents**

[TOC]

Section 1: Introduction
To display a decimal in scientific notation in Python, we can use the format() function or the f-string format.

Section 2: Using the format() function
To use the format() function, we can specify the format specifier 'e' or 'E' to represent the decimal in scientific notation.

Example code:
number = 10000.000000001
print("{:.2E}".format(number))

Output:
1.00E+04

Section 3: Using f-string format
To use f-string format, we can use the same format specifier 'e' or 'E' to represent the decimal in scientific notation.

Example code:
number = 10000.000000001
print(f"{number:.2E}")

Output:
1.00E+04

Section 4: Conclusion
Both the format() function and f-string format can be used to display a decimal in scientific notation in Python. We can use the 'e' or 'E' format specifier to get the output in scientific notation.
