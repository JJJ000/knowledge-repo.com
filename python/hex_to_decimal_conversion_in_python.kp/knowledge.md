---
title: What is the process to change hex to decimal using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the built-in int() function with the base argument set to 16.
---

**Contents**

[TOC]

Section 1: Introduction
Python is an excellent programming language with many built-in functions and libraries that can help you perform various tasks. One of the tasks you may need to perform is converting hex to decimal, and fortunately, Python has a built-in function to help you do just that.

Section 2: Using the int() function
The int() function in Python is used to convert a string or number to an integer. To convert a hexadecimal number to a decimal number using the int() function, you can provide the hexadecimal number as the first argument and 16 as the second argument. For example:

```
hex_num = "3F"
dec_num = int(hex_num, 16)
print(dec_num)
```

In this example, we convert the hexadecimal number "3F" to a decimal number using the int() function. The second argument in the int() function is the base of the number system that we want to convert from, which is 16 in this case.

Section 3: Using the built-in hex() function 
Conversely, you can also convert a decimal number to a hexidecimal numeral in Python easily using the built-in hex() function. The hexidecimal function takes a decimal number as an input and returns the equivalent string representing a hexadecimal value. For example:

```
decimal_num = 63
hex_num = hex(decimal_num)
print(hex_num)
```

In this example, 63 is the decimal number we wish to convert, and the hexadecimal representation is assigned to `hex_num`. 

Section 4: Conclusion
In conclusion, Python allows us to convert hex to decimal easily just by the in-built int() funciton. Similarly, Python allows us to convert decimal numbers to hexa-numerical representations quite easily with the in-built hex() function.
