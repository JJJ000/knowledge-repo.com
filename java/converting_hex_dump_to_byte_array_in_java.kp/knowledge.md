---
title: How can a Java program turn a string of hexadecimal values into a byte array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Integer.parseInt() method with a radix of 16 to convert each two-character substring of the hex dump string into an integer, and then use the Integer.byteValue() method to convert each integer into a byte.
---

**Contents**

[TOC]

`**` Parse the String**

The first step is to parse the string and extract the hex values. This can be done by splitting the string on any whitespace characters, such as spaces, tabs, or newlines. Then, each hex value can be parsed into a byte.

`**` Create a Byte Array**

Once the hex values have been parsed, a byte array can be created to store the values. The length of the array should be equal to the number of hex values in the string.

`**` Populate the Byte Array**

The next step is to populate the byte array with the parsed hex values. This can be done by iterating through the array of hex values and converting each one to a byte.

`**` Return the Byte Array**

Finally, the byte array can be returned. This will contain all of the parsed hex values and can be used in any application.
