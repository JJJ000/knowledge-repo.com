---
title: What is the process of turning a character into a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String constructor to create a new String object from the char.
---

**Contents**

[TOC]

### Using toString() Method
The simplest way to convert a char to a String is to use the toString() method of the Character class. This method takes a single character as an argument and returns a String object representing the character passed as argument.

Syntax:
```
public static String toString(char c)
```

Example:
```
char ch = 'A';
String str = Character.toString(ch);
```

### Using String ValueOf() Method
The String valueOf() method can also be used to convert a char to a String. This method takes a single character as an argument and returns a String object representing the character passed as argument.

Syntax:
```
public static String valueOf(char c)
```

Example:
```
char ch = 'B';
String str = String.valueOf(ch);
```

### Using StringBuilder
The StringBuilder class can also be used to convert a char to a String. This class has an append() method which takes a character as argument and appends it to the StringBuilder object.

Syntax:
```
public StringBuilder append(char c)
```

Example:
```
char ch = 'C';
StringBuilder sb = new StringBuilder();
String str = sb.append(ch).toString();
```

### Using + Operator
The + operator can also be used to convert a char to a String. This operator takes a character as an argument and concatenates it with an empty String to return a String object representing the character passed as argument.

Syntax:
```
String str = "" + ch;
```

Example:
```
char ch = 'D';
String str = "" + ch;
```
