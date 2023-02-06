---
title: Convert a Java integer into a byte array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A Java integer can be converted to a byte array using the ByteBuffer class`s putInt() method.
---

**Contents**

[TOC]

### Section 1: Converting Integer to Byte Array

Java provides a number of ways to convert an integer to a byte array. The most common way is to use the [`ByteBuffer`](https://docs.oracle.com/javase/8/docs/api/java/nio/ByteBuffer.html) class. This class provides a number of methods for converting an integer to a byte array. The `putInt()` method can be used to write an integer to a byte array, while the `get()` method can be used to read the bytes from the array.

Another way to convert an integer to a byte array is to use the [`ByteArrayOutputStream`](https://docs.oracle.com/javase/8/docs/api/java/io/ByteArrayOutputStream.html) class. This class provides methods for writing primitive data types, including integers, to an output stream. The `writeInt()` method can be used to write an integer to the output stream, and the `toByteArray()` method can be used to read the bytes from the output stream.

### Section 2: Big-Endian and Little-Endian

When converting an integer to a byte array, it is important to consider the endianness of the byte array. Endianness refers to the order of the bytes in the byte array. There are two common endianness formats: big-endian and little-endian.

In big-endian, the most significant byte is stored in the first byte of the array, while in little-endian, the least significant byte is stored in the first byte of the array. Both the `ByteBuffer` and `ByteArrayOutputStream` classes allow the endianness of the byte array to be specified when writing or reading an integer.

### Section 3: Converting Byte Array to Integer

Once an integer has been converted to a byte array, it can be converted back to an integer using the same classes. The `ByteBuffer` class provides the `getInt()` method for reading an integer from a byte array, while the `ByteArrayInputStream` class provides the `readInt()` method for reading an integer from an input stream. As with writing an integer to a byte array, the endianness of the byte array must be specified when reading an integer.

### Section 4: Summary

In summary, Java provides a number of ways to convert an integer to a byte array, including using the `ByteBuffer` and `ByteArrayOutputStream` classes. The endianness of the byte array must be specified when writing or reading an integer. Once an integer has been converted to a byte array, it can be converted back to an integer using the same classes.
