---
title: What is the best way to duplicate strings in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the String class`s .copyValueOf() or .substring() methods.
---

**Contents**

[TOC]

### Using the String Constructor

The easiest way to copy a String in Java is to use the String constructor. This constructor takes a String as an argument and returns a new String object that is a copy of the original.

```java
String originalString = "Hello World";
String copyString = new String(originalString);
```

### Using the String Copy Method

Another way to copy a String in Java is to use the String copy method. This method takes two arguments, the source String and the destination String. The method copies the characters from the source String to the destination String.

```java
String originalString = "Hello World";
String copyString = "";
copyString = originalString.copy(originalString, copyString);
```

### Using the String Concat Method

Another way to copy a String in Java is to use the String concat method. This method takes two arguments, the source String and the destination String. The method concatenates the characters from the source String to the end of the destination String.

```java
String originalString = "Hello World";
String copyString = "";
copyString = originalString.concat(originalString);
```

### Using the String Substring Method

The last way to copy a String in Java is to use the String substring method. This method takes two arguments, the start index and the end index. The method returns a new String object that is a copy of the original String starting from the start index and ending at the end index.

```java
String originalString = "Hello World";
String copyString = originalString.substring(0, originalString.length());
```
