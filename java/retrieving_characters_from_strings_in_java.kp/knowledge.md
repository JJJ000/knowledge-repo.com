---
title: Retrieve a specific character from a string using its position
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the charAt() method to get a string character by index in Java.
---

**Contents**

[TOC]

# Using charAt()
The `charAt()` method of the `String` class allows you to get a character at a specific index in a string. 

Syntax:
```
public char charAt(int index)
```

Example:
```
String str = "Hello World";
char result = str.charAt(6);
System.out.println(result);
```

Output:
```
W
```

# Using toCharArray()
The `toCharArray()` method of the `String` class allows you to convert the string into an array of characters. 

Syntax:
```
public char[] toCharArray()
```

Example:
```
String str = "Hello World";
char[] result = str.toCharArray();
System.out.println(result[6]);
```

Output:
```
W
```
