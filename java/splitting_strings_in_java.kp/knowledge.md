---
title: What is the best way to divide a string into separate parts in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `String.split()` method to split a string in Java.
---

**Contents**

[TOC]

### Using the split() Method
The split() method is used to split a string into an array of substrings, and returns the new array. 

Syntax:
```java
String[] split(String regex, int limit) 
```

Example:
```java
String str = "Hello World";
String[] arrOfStr = str.split(" ", 2); 

// arrOfStr is a string array with two elements: "Hello" and "World"
```

### Using the StringTokenizer Class
The StringTokenizer class allows an application to break a string into tokens. 

Syntax:
```java
StringTokenizer st = new StringTokenizer(String str, String delimiter) 
```

Example:
```java
String str = "Hello World";
StringTokenizer st = new StringTokenizer(str, " "); 

// st is a StringTokenizer object with two tokens: "Hello" and "World"
```

### Using the Pattern and Matcher Classes
The Pattern and Matcher classes are used to split a string into multiple tokens by specifying a regular expression (regex) as the delimiter. 

Syntax:
```java
Pattern pattern = Pattern.compile(String regex);
Matcher matcher = pattern.matcher(String str);
```

Example:
```java
String str = "Hello World";
Pattern pattern = Pattern.compile("\\s");
Matcher matcher = pattern.matcher(str);

// matcher is a Matcher object with two tokens: "Hello" and "World"
```
