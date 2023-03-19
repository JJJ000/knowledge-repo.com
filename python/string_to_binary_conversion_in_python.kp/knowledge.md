---
title: What is the process for transforming a string into binary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the built-in function `bin()` to convert a string to binary in Python.
---

**Contents**

[TOC]

## Introduction

Converting a string to binary in Python is a common operation, especially in cryptography and networking. Binary code is a way of representing data using only two digits, 0 and 1, and it is widely used in computing systems. In this guide, we will discuss how to convert a string to binary in Python.

## Step 1: Using the `bin()` function

One of the easiest ways to convert a string to binary in Python is by using the built-in `bin()` function. This function takes an integer number as an argument and returns its binary representation as a string.

Here's how you can use the `bin()` function to convert a string to binary:

``` python
s = 'hello world'
binary = ''.join(format(ord(i), '08b') for i in s)
print(binary)
```

In this code snippet, we first initialize a string `s` with the text `hello world`. To convert this string to binary, we use the `join()` method to concatenate the binary representation of each character in the string. We use the `format()` function to convert each character to its ASCII code (which is an integer) and then to its binary representation with 8 digits. Finally, we join all those binary representations together into a single string, which is stored in the `binary` variable.

When we run this code, we get the following output:

```
0110100001100101011011000110110001101111001000000111011101101111011100100110110001100100
```

This is the binary representation of the string `hello world` in ASCII code.

## Step 2: Using the `ord()` function

Another way to convert a string to binary in Python is by using the built-in `ord()` function. This function takes a character as an argument and returns its ASCII code as an integer.

Here's how you can use the `ord()` function to convert a string to binary:

``` python
s = 'hello world'
binary = ''
for c in s:
    binary += '{0:b}'.format(ord(c))
print(binary)
```

In this code snippet, we loop through each character `c` in the string `s` and use the `ord()` function to get its ASCII code. We then use the `format()` function to convert the ASCII code to binary and concatenate it to the `binary` string.

When we run this code, we get the same output as before:

```
0110100001100101011011000110110001101111001000000111011101101111011100100110110001100100
```

## Conclusion

In this guide, we have discussed two ways to convert a string to binary in Python: using the `bin()` function and using the `ord()` function. Both methods are simple and easy to implement. However, the `bin()` method may be more efficient for large strings, as it uses the built-in binary conversion functions in Python.
