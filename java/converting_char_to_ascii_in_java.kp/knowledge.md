---
title: Change a character to its corresponding ascii code number in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In Java, the Character class has a method called `getNumericValue()` which returns the ASCII numeric value of a character.
---

**Contents**

[TOC]

# Using Character.getNumericValue()
The `Character.getNumericValue()` method is used to get the Unicode numeric value of the character.

Syntax:
`public static int getNumericValue(char ch)`

Example:
```java
public class Main {
    public static void main(String[] args) {
        char ch = 'A';
        int asciiValue = Character.getNumericValue(ch);
        System.out.println("ASCII value of character " + ch + " is: " + asciiValue);
    }
}
```

Output:
```
ASCII value of character A is: 10
```

# Using typecasting
The ASCII value of a character can also be obtained by typecasting.

Syntax:
`int asciiValue = (int) charValue`

Example:
```java
public class Main {
    public static void main(String[] args) {
        char ch = 'A';
        int asciiValue = (int) ch;
        System.out.println("ASCII value of character " + ch + " is: " + asciiValue);
    }
}
```

Output:
```
ASCII value of character A is: 65
```
