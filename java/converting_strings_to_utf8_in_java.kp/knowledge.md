---
title: What is the process of translating strings to and from utf8 byte arrays in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String constructor with a byte array argument and the getBytes() method to convert Strings to and from UTF8 byte arrays in Java.
---

**Contents**

[TOC]

# Section 1 - Converting Strings to UTF8 Byte Arrays

The easiest way to convert a String to a UTF8 byte array is to use the `getBytes()` method. This method takes in an optional argument, which is the character encoding for the returned byte array. By default, it uses the system's default character encoding, but it can be easily changed to UTF-8 by passing in the `"UTF-8"` argument.

```java
String str = "Hello World!";
byte[] bytes = str.getBytes("UTF-8");
```

# Section 2 - Converting UTF8 Byte Arrays to Strings

The easiest way to convert a UTF8 byte array to a String is to use the `String` constructor. This constructor takes in a byte array and an optional argument, which is the character encoding for the byte array. By default, it uses the system's default character encoding, but it can be easily changed to UTF-8 by passing in the `"UTF-8"` argument.

```java
byte[] bytes = {...};
String str = new String(bytes, "UTF-8");
```

# Section 3 - Character Encoding

Character encoding is a system used to convert a sequence of characters (such as a String) into a sequence of bytes (such as a byte array). Different character encodings can be used to represent the same sequence of characters in different ways. UTF-8 is a popular encoding that is used for web pages and other text-based communication.

# Section 4 - Further Reading

For more information on character encoding, see the following resources:

* [Wikipedia article on Character Encoding](https://en.wikipedia.org/wiki/Character_encoding)
* [Java Tutorials - Character Encoding](https://docs.oracle.com/javase/tutorial/i18n/text/string.html)
