---
title: What is the process for transforming a byte array to a hexadecimal string in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.format() method with the `%02x` format specifier to convert a byte array to a hex string.
---

**Contents**

[TOC]

### Overview

A byte array can be converted to a hex string in Java by using the `String.format()` method with a `%x` format specifier.

### Steps

1. Create a `StringBuilder` object.
2. Iterate through the byte array and append the hexadecimal representation of each byte to the `StringBuilder` object.
3. Use the `String.format()` method to format the `StringBuilder` object as a hex string.

### Example

The following example converts a byte array to a hex string:

```java
byte[] bytes = { 0x0A, 0x0B, 0x0C };

StringBuilder sb = new StringBuilder();
for (byte b : bytes) {
    sb.append(String.format("%x", b));
}
String hexString = sb.toString();
// hexString = "a0b0c"
```

### Further Reading

For more information about the `String.format()` method, see the [JavaDoc](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html#format-java.lang.String-java.lang.Object...-) documentation.
