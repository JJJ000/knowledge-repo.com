---
title: What is the syntax for extracting the file name without the extension in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String class`s substring() method to get the filename without the extension.
---

**Contents**

[TOC]

### Solution 1: Using substring()

1. Get the index of the last occurrence of the ‘.’ character in the String using lastIndexOf() method. 
2. Use substring() method to get the substring from 0 index to the index of last occurrence of the ‘.’ character.
3. The substring will be the filename without the extension.

### Solution 2: Using split()

1. Split the String using ‘.’ as the delimiter using split() method.
2. The first element of the returned array will be the filename without the extension.
