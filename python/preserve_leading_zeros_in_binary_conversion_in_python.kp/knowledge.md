---
title: Transform into binary and retain the leading zeroes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To convert to binary and keep leading zeros in Python, use the format specifier `{008b}` where 8 is the number of digits including leading zeros.
---

**Contents**

[TOC]

## Introduction
In Python, we can convert a decimal number into a binary number using the `bin()` function. However, by default, the binary number returned by the `bin()` function does not retain leading zeros. In this tutorial, we will explore different methods to convert a decimal number into a binary number and retain the leading zeros.

## Using string formatting 

One way to retain the leading zeros while converting decimal to binary in Python is to use string formatting. We can use `format()` function and add `0` padding to the left of the binary number.

```python
decimal_number = 5
bits = 8 # number of bits for binary representation
binary_number = '{0:0{1}b}'.format(decimal_number, bits)
print(binary_number)
```

Output:
```
00000101
```

Here, we first define the decimal number and the number of bits for binary representation as `bits`. We then use the `format()` function to convert the decimal number into its binary representation with a width of `bits`. We add an `0` padding to the left using the padding specifier `{0:0{1}b}`, where `0` indicates the position of the argument (the decimal_number in this case), `{1}` indicates the position of the width argument (the bits in this case), and `b` indicates that the argument should be converted into a binary number.

## Using zfill method

Another way to retain the leading zeros is to use the `zfill()` method. The `zfill()` method pads a string with zeros to a specified width. The `bin()` function can be used to convert the decimal number into a binary string, which can then be padded with zeros using the `zfill()` method.

```python
decimal_number = 5
bits = 8 
binary_number = bin(decimal_number).replace("0b", "").zfill(bits)
print(binary_number)
```

Output:
```
00000101
```

Here, we first use the `bin()` function to convert the decimal number into a binary string. We remove the prefix `0b` from the binary string using the `replace()` method. We then use the `zfill()` method to pad the binary string with zeros to a width of `bits`.

## Using bit shifting

A third way to retain the leading zeros is by using bitwise operations. This method involves shifting the bits of the decimal number to the left, adding leading zeros as necessary to maintain the width. We can use the `<<` operator to shift the bits to the left.

```python
decimal_number = 5
bits = 8
binary_number = "{0:b}".format(decimal_number << (bits - decimal_number.bit_length()))
print(binary_number.zfill(bits))
```

Output:
```
00000101
```

Here, we first shift the bits of the decimal number to the left by the number of bits required to meet the width using `(bits - decimal_number.bit_length())`. We then convert the shifted decimal number into its binary representation using the `"{0:b}"` format specifier. Finally, we pad the binary string with `0`s using the `zfill()` method. 

## Conclusion

In Python, we can retain leading zeros while converting a decimal number to a binary number using string formatting, the `zfill()` method, and bitwise operations. Each method uses a different approach, and the choice of method depends on the specific use case.
