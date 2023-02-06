---
title: What is the syntax for capitalizing the first letter of each word in a string using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String.replaceFirst() method to replace the first character of the string with its capitalized equivalent.
---

**Contents**

[TOC]

### Section 1: Split the String

The first step is to split the string into individual words. This can be done by using the `split()` method of the `String` class.

### Section 2: Capitalize the First Letter

Once the string has been split, the first letter of each word can be capitalized using the `substring()` and `toUpperCase()` methods of the `String` class.

### Section 3: Reconstruct the String

Once the first letter of each word has been capitalized, the words can be reconstructed into a single string using the `StringBuilder` class.

### Section 4: Return the Capitalized String

Finally, the capitalized string can be returned using the `toString()` method of the `StringBuilder` class.
