---
title: Does anyone know how to convert a string to and from base64 using base64 encoding?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To decode and encode a string in Base64 using Base64 in Java, use the getDecoder() and getEncoder() methods of the java.util.Base64 class.
---

**Contents**

[TOC]

**Encoding a String in Base64**

1. Create a String object with the desired text.

2. Create a Base64 object with the getEncoder().

3. Use the encode() method of the Base64 object to encode the String object.

4. Store the encoded string in a new String object.

**Decoding a String in Base64**

1. Create a String object with the encoded text.

2. Create a Base64 object with the getDecoder().

3. Use the decode() method of the Base64 object to decode the String object.

4. Store the decoded string in a new String object.
