---
title: Decode base64 information using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Base64 data can be decoded in Java using the java.util.Base64 class.
---

**Contents**

[TOC]

### Introduction
Base64 is a binary-to-text encoding scheme that is used to represent binary data in an ASCII string format. It is used to encode data in emails, web pages, and other online applications. In Java, Base64 can be decoded using the java.util.Base64 class.

### Decoding Base64
The java.util.Base64 class provides the static decode() method for decoding a Base64 encoded string. This method takes a single argument, which is the Base64 encoded string, and returns a byte array containing the decoded data.

### Example
The following example shows how to decode a Base64 encoded string in Java:

```java
String encodedString = "dGVzdA==";
byte[] decodedBytes = Base64.decode(encodedString);
String decodedString = new String(decodedBytes);
System.out.println(decodedString); // prints "test"
```

### Conclusion
Decoding Base64 data in Java is a simple process using the java.util.Base64 class. The decode() method takes a single argument, which is the Base64 encoded string, and returns a byte array containing the decoded data.
