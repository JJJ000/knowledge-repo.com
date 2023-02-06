---
title: Retrieve numerical values from a string in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the regex pattern `[0-9]+` and the String method replaceAll() to extract all digits from a string in Java.
---

**Contents**

[TOC]

### Using Regular Expressions 

Java provides the `java.util.regex` package for creating and manipulating regular expressions. Using this package, we can create a regular expression to extract digits from a string. 

The following code snippet demonstrates how to use regular expressions to extract digits from a string:

```java
String str = "Hello123World456";
Pattern p = Pattern.compile("\\d+");
Matcher m = p.matcher(str);
while (m.find()) {
    System.out.println(m.group());
}
```

### Using Character Class

Java also provides the `Character` class for working with characters. This class has a `isDigit()` method which can be used to check if a character is a digit or not. 

The following code snippet demonstrates how to use the `Character` class to extract digits from a string:

```java
String str = "Hello123World456";
StringBuilder sb = new StringBuilder();
for (int i = 0; i < str.length(); i++) {
    if (Character.isDigit(str.charAt(i))) {
        sb.append(str.charAt(i));
    }
}
System.out.println(sb.toString());
```

### Using Java 8 Streams 

Java 8 provides the `Stream` API for working with collections of objects. This API can be used to extract digits from a string by mapping each character of the string to a `Character` object and then filtering out the digits using the `isDigit()` method.

The following code snippet demonstrates how to use Java 8 streams to extract digits from a string:

```java
String str = "Hello123World456";
String digits = str.chars()
    .mapToObj(c -> (char) c)
    .filter(Character::isDigit)
    .collect(StringBuilder::new,
        StringBuilder::append,
        StringBuilder::append)
    .toString();
System.out.println(digits);
```
