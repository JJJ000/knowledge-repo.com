---
title: Determine if a Java enumeration includes a specific string value
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the Enum.contains() method to check if an enum contains a given string.
---

**Contents**

[TOC]

## Option 1: Using Enum.valueOf()

Java provides a `valueOf()` method for enum types that can be used to check if an enum contains a given string. The method takes a single string argument and returns the corresponding enum constant. If the string does not match any of the enum constants, then a `IllegalArgumentException` will be thrown. 

Example: 

```java
public enum Color {
    RED, GREEN, BLUE;
}

// Check if the enum contains "RED"
try {
    Color color = Color.valueOf("RED");
    System.out.println("Enum contains RED");
} catch (IllegalArgumentException e) {
    System.out.println("Enum does not contain RED");
}
```

## Option 2: Using Enum.values()

Java also provides an `values()` method for enum types that can be used to check if an enum contains a given string. The method returns an array of all the enum constants. This array can then be iterated over to check if the given string matches any of the enum constants.

Example: 

```java
public enum Color {
    RED, GREEN, BLUE;
}

// Check if the enum contains "RED"
boolean containsRed = false;
for (Color color : Color.values()) {
    if (color.name().equals("RED")) {
        containsRed = true;
        break;
    }
}
System.out.println("Enum contains RED: " + containsRed);
```

## Option 3: Using Enum.stream()

Java 8 introduced the `stream()` method for enum types that can be used to check if an enum contains a given string. The method returns a stream of all the enum constants. This stream can then be filtered to check if the given string matches any of the enum constants.

Example: 

```java
public enum Color {
    RED, GREEN, BLUE;
}

// Check if the enum contains "RED"
boolean containsRed = Color.stream()
    .anyMatch(color -> color.name().equals("RED"));
System.out.println("Enum contains RED: " + containsRed);
```

## Option 4: Using Arrays.stream()

Java 8 also introduced the `Arrays.stream()` method for arrays that can be used to check if an enum contains a given string. The method takes an array of objects and returns a stream of the objects. This stream can then be filtered to check if the given string matches any of the enum constants.

Example: 

```java
public enum Color {
    RED, GREEN, BLUE;
}

// Check if the enum contains "RED"
boolean containsRed = Arrays.stream(Color.values())
    .anyMatch(color -> color.name().equals("RED"));
System.out.println("Enum contains RED: " + containsRed);
```
