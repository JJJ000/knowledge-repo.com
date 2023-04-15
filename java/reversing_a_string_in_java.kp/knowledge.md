---
title: In java, how to reverse the order of characters in a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To reverse a string in Java, use the StringBuilder class and its reverse() method.
---

**Contents**

[TOC]

`**` Using a for loop**

```java
public static String reverseString(String str) {
    String reversedString = "";
    for (int i = str.length() - 1; i >= 0; i--) {
        reversedString += str.charAt(i);
    }
    return reversedString;
}
```

`**` Using the StringBuilder class**

```java
public static String reverseString(String str) {
    StringBuilder sb = new StringBuilder();
    for (int i = str.length() - 1; i >= 0; i--) {
        sb.append(str.charAt(i));
    }
    return sb.toString();
}
```

`**` Using the StringBuffer class**

```java
public static String reverseString(String str) {
    StringBuffer sb = new StringBuffer();
    for (int i = str.length() - 1; i >= 0; i--) {
        sb.append(str.charAt(i));
    }
    return sb.toString();
}
```

`**` Using recursion**

```java
public static String reverseString(String str) {
    if (str.length() == 1) {
        return str;
    }
    return reverseString(str.substring(1)) + str.charAt(0);
}
```
