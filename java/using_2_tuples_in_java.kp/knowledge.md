---
title: Working with pairs or 2-tuples in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pairs or 2-tuples in Java can be represented using the java.util.AbstractMap.SimpleEntry class.
---

**Contents**

[TOC]

### Introduction

Pairs, or 2-tuples, are a data structure in Java that can hold two values of different data types. They are useful for storing related data that should be kept together, such as a key-value pair. Pairs can be used to store information that would normally be stored in separate variables, such as a person’s first and last name. 

### Creating a Pair

Pairs can be created by using the Java `Pair` class. This class can be imported from the `org.apache.commons.lang3.tuple` package. To create a pair, the two values must be specified as arguments in the constructor. For example, to create a pair containing the strings "John" and "Smith", the following code can be used: 

```java
Pair<String, String> name = new Pair<String, String>("John", "Smith");
```

### Accessing Values

Once the pair has been created, the values can be accessed using the `getLeft()` and `getRight()` methods. For example: 

```java
String firstName = name.getLeft(); // firstName is now "John"
String lastName = name.getRight(); // lastName is now "Smith"
```

### Conclusion

Pairs are a useful data structure in Java for storing related data. They can be created using the `Pair` class and the values can be accessed using the `getLeft()` and `getRight()` methods.
