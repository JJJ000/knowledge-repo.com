---
title: What is the process of changing a color integer to a hexadecimal string in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String.format() method with the format string `%X` to convert a color integer to a hex String in Android.
---

**Contents**

[TOC]

## Solution 1

1. Create a `StringBuilder` object.
2. Get the red, green, and blue components from the color integer by using the `Color` class's `red`, `green`, and `blue` methods.
3. Append the hex representation of each component to the `StringBuilder` object.
4. Finally, call the `toString` method on the `StringBuilder` object to get the hex String.

## Solution 2

1. Create a `String` object and set it to an empty string.
2. Get the red, green, and blue components from the color integer by using the `Color` class's `red`, `green`, and `blue` methods.
3. Append the hex representation of each component to the `String` object.
4. Finally, call the `toUpperCase` method on the `String` object to get the hex String.
