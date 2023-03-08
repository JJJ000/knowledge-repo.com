---
title: How can I write a Python code to change a decimal number to binary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To convert decimal to binary in Python, use the built-in `bin()` function.
---

**Contents**

[TOC]

## Using the bin() function
In python, the easiest way to convert decimal to binary is to use the built-in `bin()` function. This function takes an integer as its argument and returns its binary representation as a string.

```python
decimal_num = 10
binary_num = bin(decimal_num)
print(binary_num)
```
Output: `0b1010`

Note that the output includes the prefix `0b`, which indicates that the number is in binary form.

To get rid of this prefix, you can use string slicing as follows:

```python
binary_num = bin(decimal_num)[2:]
print(binary_num)
```
Output: `1010`

## Using the format() function
Another way to convert a decimal number to binary is to use the `format()` function, which allows you to specify the format of a string.

```python
decimal_num = 10
binary_num = format(decimal_num, 'b')
print(binary_num)
```
Output: `1010`

In this example, the second argument to the `format()` function is the format specifier `'b'`, which tells python to format the number as binary.

## Using recursive function
We can also convert decimal to binary by implementing a recursive function in python. The function takes an integer as its parameter and returns its binary representation as a string.

```python
def decimal_to_binary(decimal_num):
    if decimal_num == 0:
        return '0'
    elif decimal_num == 1:
        return '1'
    else:
        return decimal_to_binary(decimal_num // 2) + str(decimal_num % 2)


decimal_num = 10
binary_num = decimal_to_binary(decimal_num)
print(binary_num)
```
Output: `1010`

In this implementation, the function recursively calls itself to compute the binary representation of the number. The base case is when the number is either 0 or 1, in which case it returns the string `'0'` or `'1'`, respectively. For all other numbers, it recursively calls itself with the integer quotient of the number divided by 2 and the remainder of the number mod 2, concatenating the result to the end of the string.
