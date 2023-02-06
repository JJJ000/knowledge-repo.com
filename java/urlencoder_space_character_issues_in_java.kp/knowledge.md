---
title: The urlencoder is unable to encode a space character
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, URLEncoder cannot directly encode space characters; they must be encoded as `%20`.
---

**Contents**

[TOC]

# Introduction
URL encoding is a process of encoding a string so that it can be transmitted over the internet as a valid URL. It is used to convert special characters into a valid URL format. The most common character that needs to be encoded is the space character, which is represented by the '%20' code.

# Problem
The java.net.URLEncoder class is used to encode a string into a valid URL format. However, it is not able to translate the space character into the '%20' code. This means that a space character in the string will remain as a space character when it is encoded.

# Solution
The solution is to use the java.net.URLEncoder.encode(String s, String encoding) method instead. This method takes two parameters, the string to be encoded and the encoding type. The encoding type should be set to “UTF-8”. This method will properly encode the space character into the '%20' code.

# Conclusion
The java.net.URLEncoder class is not able to properly encode the space character into the '%20' code. The solution is to use the java.net.URLEncoder.encode(String s, String encoding) method instead, with the encoding type set to “UTF-8”. This will properly encode the space character into the '%20' code.
