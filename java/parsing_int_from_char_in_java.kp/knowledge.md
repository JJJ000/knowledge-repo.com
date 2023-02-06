---
title: Convert a character to an integer value in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the Character class`s static method `getNumericValue(char c)` to parse an int value from a char.
---

**Contents**

[TOC]

## Solution

### Using Character.getNumericValue()

The `Character.getNumericValue()` method can be used to parse an int value from a char. This method returns the int value of the char argument.

Example:

```java
char c = '2';
int i = Character.getNumericValue(c);
System.out.println(i); // prints 2
```

### Using Integer.parseInt()

The `Integer.parseInt()` method can also be used to parse an int value from a char. This method parses the string argument as a signed decimal integer.

Example:

```java
char c = '2';
String s = Character.toString(c);
int i = Integer.parseInt(s);
System.out.println(i); // prints 2
```

### Using Integer.valueOf()

The `Integer.valueOf()` method can also be used to parse an int value from a char. This method returns an Integer object holding the value of the specified string.

Example:

```java
char c = '2';
String s = Character.toString(c);
Integer i = Integer.valueOf(s);
System.out.println(i); // prints 2
```

### Using Integer.decode()

The `Integer.decode()` method can also be used to parse an int value from a char. This method decodes a string into an integer.

Example:

```java
char c = '2';
String s = Character.toString(c);
Integer i = Integer.decode(s);
System.out.println(i); // prints 2
```
