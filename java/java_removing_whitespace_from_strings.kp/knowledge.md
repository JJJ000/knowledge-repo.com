---
title: Eliminating whitespace from strings in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Strings can be trimmed of whitespace in Java using the trim() method.
---

**Contents**

[TOC]

### Using the trim() Method
The trim() method removes leading and trailing whitespace from a string. It can be used as follows:

```java
String myString = "   My String    ";
myString = myString.trim();
System.out.println(myString); // Outputs: "My String"
```

### Using Regular Expressions
Regular expressions can be used to remove all whitespace from a string. This can be done using the following code:

```java
String myString = "   My String    ";
myString = myString.replaceAll("\\s+","");
System.out.println(myString); // Outputs: "MyString"
```

### Using StringUtils from Apache Commons
The StringUtils class from the Apache Commons library can also be used to remove whitespace from a string. This can be done using the following code:

```java
String myString = "   My String    ";
myString = StringUtils.deleteWhitespace(myString);
System.out.println(myString); // Outputs: "MyString"
```

### Using the replace() Method
The replace() method can also be used to remove whitespace from a string. This can be done using the following code:

```java
String myString = "   My String    ";
myString = myString.replace(" ", "");
System.out.println(myString); // Outputs: "MyString"
```
