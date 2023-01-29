---
title: What is the distinction between the string replace() and replaceall() methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: String replace() replaces all occurrences of a specified character or string with another character or string, while replaceAll() replaces a specified regular expression with a replacement string.
---

**Contents**

[TOC]

### String replace()
`String replace()` is a method of the String class in Java which is used to replace a character or a substring of the String with a new character or substring. This method takes two parameters, the old character or substring which needs to be replaced and the new character or substring which will be used to replace the old one. It returns a new String object with all occurrences of the old character or substring replaced with the new one.

### String replaceAll()
`String replaceAll()` is a method of the String class in Java which is used to replace all occurrences of a regular expression (regex) with a new character or substring. This method takes two parameters, the regex which needs to be replaced and the new character or substring which will be used to replace the regex. It returns a new String object with all occurrences of the regex replaced with the new one.

### Difference
The main difference between `String replace()` and `String replaceAll()` is that `String replace()` replaces only a character or substring while `String replaceAll()` replaces a regular expression (regex). Another difference is that `String replace()` is faster than `String replaceAll()` since it does not need to parse the regex.
