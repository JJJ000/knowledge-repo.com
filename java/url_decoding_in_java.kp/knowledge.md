---
title: What is the process for decoding urls in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: URL decoding can be done in Java using the URLDecoder.decode() method.
---

**Contents**

[TOC]

### Overview
URL decoding is the process of transforming encoded strings into their original form. The encoded string is usually in the form of a percent-encoded string, which is a string of characters that have been replaced with a percent sign (%) followed by two hexadecimal digits. URL decoding can be done in Java using the java.net.URLDecoder class.

### Setting Up
To use the java.net.URLDecoder class, you must first import it into your program. This can be done by adding the following line of code to the beginning of your program:

`import java.net.URLDecoder;`

### Implementing
Once the java.net.URLDecoder class is imported, you can use the `decode` method to decode a percent-encoded string. This method takes the encoded string as a parameter and returns the decoded string. For example, the following code will decode a percent-encoded string:

`String decodedString = URLDecoder.decode(encodedString);`

### Conclusion
URL decoding in Java can be done using the java.net.URLDecoder class. To use this class, you must first import it into your program. Once imported, you can use the `decode` method to decode a percent-encoded string.
