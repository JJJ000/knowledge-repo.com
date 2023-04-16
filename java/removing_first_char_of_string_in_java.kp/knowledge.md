---
title: Removing the initial character of a string in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the substring() method to remove the first character of a String.
---

**Contents**

[TOC]

**1. Using substring() Method**

The `substring()` method can be used to remove the first character of a string. The `substring()` method takes two parameters: the start index and the end index. To remove the first character, the start index should be 1 and the end index should be the length of the string.

**2. Using replaceFirst() Method**

The `replaceFirst()` method can also be used to remove the first character of a string. The `replaceFirst()` method takes two parameters: a regular expression and a replacement string. To remove the first character, the regular expression should be `^.` (which matches the first character) and the replacement string should be empty.

**3. Using deleteCharAt() Method**

The `deleteCharAt()` method can be used to remove the first character of a string. The `deleteCharAt()` method takes one parameter: the index of the character to be deleted. To remove the first character, the index should be 0.

**4. Using a Character Array**

A character array can also be used to remove the first character of a string. The string can be converted to a character array using the `toCharArray()` method. Then, a new character array can be created without the first character. Finally, the new character array can be converted back to a string using the `String.valueOf()` method.
