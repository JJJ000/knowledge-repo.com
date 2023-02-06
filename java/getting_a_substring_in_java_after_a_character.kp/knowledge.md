---
title: Obtaining a substring from a string beginning after a specified character in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the substring() method, passing in the index of the character to start after as the first argument and the index of the last character to include as the second argument.
---

**Contents**

[TOC]

1. **Identifying the Character**
The first step is to identify the character that the desired substring will start after. This can be done by using the indexOf() method, which returns the index of the first occurrence of a specified character in a string. 

2. **Creating a Substring**
Once the character has been identified, the substring can be created using the substring() method. This method takes two parameters: the starting index of the desired substring and the ending index. The starting index should be the index of the character found in the first step plus one. The ending index can be left blank to get the rest of the string.

3. **Using the Substring**
The substring can now be used in whatever way is needed. It can be printed, assigned to a variable, or used in a calculation. 

4. **Example**
For example, if the string is "Hello World!" and the desired substring starts after the space character, the following code can be used:

```
String str = "Hello World!";
int index = str.indexOf(" ");
String substring = str.substring(index + 1);
System.out.println(substring);
```

This code will print out "World!".
