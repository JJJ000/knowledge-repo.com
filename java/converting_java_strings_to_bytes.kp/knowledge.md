---
title: What is the process for changing a Java string into a byte array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the getBytes() method to convert a Java String into a byte[].
---

**Contents**

[TOC]

1. **Creating a Byte Array from a String**

To convert a Java String into a byte array, you can use the `getBytes()` method of the String class. This method returns a byte array containing the characters of the String encoded using the platform's default charset.

2. **Using a Specific Charset**

If you want to convert the String using a specific charset, you can use the `getBytes(Charset charset)` method of the String class. This method returns a byte array containing the characters of the String encoded using the specified charset.

3. **Using a Specific Encoding**

If you want to convert the String using a specific encoding, you can use the `getBytes(String encoding)` method of the String class. This method returns a byte array containing the characters of the String encoded using the specified encoding.

4. **Converting a Byte Array to a String**

To convert a byte array back into a String, you can use the `String(byte[] bytes)` constructor of the String class. This constructor creates a new String object from the specified byte array.
