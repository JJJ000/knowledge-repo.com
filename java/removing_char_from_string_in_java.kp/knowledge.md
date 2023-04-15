---
title: Take out all instances of char from string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: String.replaceAll(String regex, String replacement) can be used to remove all occurrences of a character from a string.
---

**Contents**

[TOC]

**Solution 1: Using for loop**

```java
public static String removeChar(String str, char ch) 
{ 
    String result = ""; 
    for (int i = 0; i < str.length(); i++) { 
        char currentChar = str.charAt(i); 
        if (currentChar != ch) { 
            result += currentChar; 
        } 
    } 
    return result; 
} 
```

**Solution 2: Using replaceAll() method**

```java
public static String removeChar(String str, char ch) 
{ 
    return str.replaceAll(Character.toString(ch), ""); 
} 
```

**Solution 3: Using replace() method**

```java
public static String removeChar(String str, char ch) 
{ 
    StringBuilder sb = new StringBuilder(); 
    for (int i = 0; i < str.length(); i++) { 
        char currentChar = str.charAt(i); 
        if (currentChar != ch) { 
            sb.append(currentChar); 
        } 
    } 
    return sb.toString(); 
} 
```

**Solution 4: Using StringBuffer**

```java
public static String removeChar(String str, char ch) 
{ 
    StringBuffer sb = new StringBuffer(); 
    for (int i = 0; i < str.length(); i++) { 
        char currentChar = str.charAt(i); 
        if (currentChar != ch) { 
            sb.append(currentChar); 
        } 
    } 
    return sb.toString(); 
} 
```
