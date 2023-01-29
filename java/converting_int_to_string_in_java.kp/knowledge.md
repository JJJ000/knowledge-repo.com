---
title: What is the process for changing an integer to a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To convert an int to a String in Java, use the String.valueOf() method.
---

**Contents**

[TOC]

### Using the toString() Method

The simplest way to convert an int to a String is to use the toString() method of the Integer class. The toString() method takes an int value as its parameter and returns a String object representing the int parameter.

Example:
```
int number = 42;
String numberString = Integer.toString(number);
```

### Using the String.valueOf() Method

Another way to convert an int to a String is to use the String.valueOf() method. This method takes an int value as its parameter and returns a String object representing the int parameter.

Example:
```
int number = 42;
String numberString = String.valueOf(number);
```

### Using the String Constructor

You can also use the String constructor to convert an int to a String. The String constructor takes an int value as its parameter and returns a String object representing the int parameter.

Example:
```
int number = 42;
String numberString = new String(number);
```

### Using the StringBuilder

Finally, you can use the StringBuilder class to convert an int to a String. The StringBuilder class has an append() method which takes an int value as its parameter and returns a String object representing the int parameter.

Example:
```
int number = 42;
StringBuilder sb = new StringBuilder();
String numberString = sb.append(number).toString();
```
