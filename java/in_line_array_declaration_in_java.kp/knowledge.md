---
title: Is there a way to create an array without writing out each element?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, an array can be declared in-line in Java using the syntax `type[] arrayName = {value1, value2, ...};`.
---

**Contents**

[TOC]

### Option 1: Array Initialization

Java allows you to declare an array in-line by using the array initialization syntax. This syntax allows you to specify the elements of the array directly in the declaration.

For example:

```java
int[] array = {1,2,3,4,5};
```

### Option 2: Array Literal

Another option for declaring an array in-line is to use an array literal. An array literal is a shorthand notation for creating an array with elements of the same type.

For example:

```java
int[] array = new int[] {1,2,3,4,5};
```

### Option 3: Array Creation Expressions

Another way to declare an array in-line is to use array creation expressions. This syntax allows you to specify the size of the array and the type of the elements in the array.

For example:

```java
int[] array = new int[5];
```

### Option 4: Anonymous Array

The last option for declaring an array in-line is to use an anonymous array. This syntax allows you to create an array without giving it a name.

For example:

```java
new int[] {1,2,3,4,5};
```
