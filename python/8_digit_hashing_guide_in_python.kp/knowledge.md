---
title: What is the process of converting a string into 8-digit hash?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: You can hash a string into 8 digits in Python using the built-in function `hash()` and then getting the last 8 digits using modulo operator.
---

**Contents**

[TOC]

### Introduction

Hashing is the process of converting input data (in our case, a string) into a fixed-size, usually one-way encoded output. In this tutorial, we will learn how to hash a string into 8 digits in Python.

### Method 1: Using the hash() function

The hash() function in Python is used to generate a unique integer hash value of an object. We can use this function to hash a string into an integer value, and then convert this integer value into an 8 digit number using a modulo operation.

```python
def hash_string(s):
    h = hash(s)
    return abs(h) % (10 ** 8)
```

In the above code, we use the hash() function to generate a hash value of the input string 's'. We then take the absolute value of this hash value (since it may be negative), and use a modulo operation to convert it to an 8 digit number.

### Method 2: Using the hashlib library

The hashlib library in Python provides more secure hash functions than the built-in hash() function. We can use the hashlib library to generate a hash value of a string, and then convert this hash value into an 8 digit number using the same modulo operation as before.

```python
import hashlib

def hash_string(s):
    h = hashlib.sha256(s.encode()).hexdigest()
    return int(h, 16) % (10 ** 8)
```

In the above code, we use the SHA-256 hash function from the hashlib library to generate a hash value of the input string 's'. We then use the hexdigest() method to convert this hash value to a hexadecimal string, and convert this hexadecimal string to an integer using the int() function with a base of 16. Finally, we use the same modulo operation as before to convert this integer into an 8 digit number.

### Conclusion

In this tutorial, we have learned two methods to hash a string into 8 digits in Python. The first method uses the built-in hash() function, while the second method uses the more secure hash functions provided by the hashlib library. Depending on the level of security required, one method may be preferable over the other.
