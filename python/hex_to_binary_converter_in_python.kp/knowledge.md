---
title: Transform hexadecimal code to binary format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert hex to binary in Python, use the built-in function bin(int(hex\_value,16)) where hex\_value is the hex string.
---

**Contents**

[TOC]

# Introduction
Hexadecimal (hex) and binary are two commonly used number systems in computer science. Hexadecimal is a base-16 numeral system used to represent numbers. Binary, on the other hand, is a base-2 numeral system used for digital electronics and computing. Converting a given hex number to binary is a common task in programming. Luckily, Python offers several built-in functions and methods that can help us perform this task easily.

# Using the bin() Function
The easiest and most straightforward way to convert a hex number to binary in Python is by using the built-in `bin()` function. Here's the syntax of the function:

```
bin(number)
```

Here, `number` is the hex number that we want to convert to binary. The `bin()` function returns the binary equivalent of the given number in the form of a string.

Let's take an example: Suppose we want to convert the hex number `0x1a` to binary. We can do it using the `bin()` function as follows:

```python
hex_num = 0x1a
binary_num = bin(hex_num)
print(binary_num)
```

This will output:

```
0b11010
```

Here, `0b` is a prefix that indicates that the resulting number is in binary form.

# Using the format() Method
Another way to convert a hex number to binary in Python is by using the `format()` method. Here's the syntax of the method:

```
format(number, 'b')
```

Here, `number` is the hex number that we want to convert to binary, and the second argument `'b'` tells the `format()` method that we want the binary equivalent of the number.

Let's take the same example as before:

```python
hex_num = 0x1a
binary_num = format(hex_num, 'b')
print(binary_num)
```

This will output the same binary number as before:

```
11010
```

Note that there is no prefix `0b` in the output.

# Using a Custom Function
Finally, we can also write a custom function to convert a hex number to binary in Python. Here is one way to do it:

```python
def hex_to_binary(hex_num):
    decimal_num = int(hex_num, 16)
    binary_num = bin(decimal_num)[2:]
    return binary_num
```

Here, we first convert the hex number to its decimal equivalent using the `int()` function. Then, we use the `bin()` function to convert the decimal number to binary. The `[2:]` at the end of the `bin()` function call is to remove the prefix `0b` from the resulting binary string.

We can use this function as follows:

```python
hex_num = '1a'
binary_num = hex_to_binary(hex_num)
print(binary_num)
```

This will output the same binary number as before:

```
11010
```

# Conclusion
Python provides several ways to convert a hex number to binary, including using the `bin()` function, the `format()` method, or a custom function. You can choose the one that best fits your needs and preferences.
