---
title: What is the process for changing a long data type to an int data type in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the intValue() method on the Long object to convert a Long to an int.
---

**Contents**

[TOC]

### Using Integer.parseInt()

The `Integer.parseInt()` method can be used to convert a long to an int. This method takes a `String` as an argument and returns an `int` value.

```java
long l = 123456789;
int i = Integer.parseInt(Long.toString(l));
```

### Using Long.intValue()

The `Long.intValue()` method can be used to convert a long to an int. This method returns an `int` value which is the result of the conversion.

```java
long l = 123456789;
int i = l.intValue();
```

### Using Math.toIntExact()

The `Math.toIntExact()` method can be used to convert a long to an int. This method takes a `long` as an argument and returns an `int` value.

```java
long l = 123456789;
int i = Math.toIntExact(l);
```

### Using Casting 

The `(int)` operator can be used to convert a long to an int. This operator takes a `long` as an argument and returns an `int` value.

```java
long l = 123456789;
int i = (int) l;
```
