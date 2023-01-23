---
title: What is the easiest way to output a Java array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: The simplest way to print a Java array is to use the `Arrays.toString()` method.
---

**Contents**

[TOC]

### Using a Loop

The simplest way to print a Java array is to use a loop. Loops allow you to iterate through each element of the array, and print them one by one. The following example uses a for loop to print out every element of an array of integers:

```java
int[] array = {1, 2, 3, 4, 5};

for (int i = 0; i < array.length; i++) {
    System.out.println(array[i]);
}
```

### Using the Arrays Class

The Arrays class in Java provides a static method called `toString()` which can be used to print out the contents of an array. The following example uses the `toString()` method to print out the contents of an array of strings:

```java
String[] array = {"a", "b", "c", "d"};

System.out.println(Arrays.toString(array));
```

### Using the Stream API

The Stream API in Java 8 provides a convenient way to print out the contents of an array. The following example uses the `forEach()` method to print out every element of an array of integers:

```java
int[] array = {1, 2, 3, 4, 5};

Arrays.stream(array).forEach(System.out::println);
```

### Using the toString() Method

The `toString()` method can also be used to print out the contents of an array. The following example uses the `toString()` method to print out the contents of an array of strings:

```java
String[] array = {"a", "b", "c", "d"};

System.out.println(array.toString());
```
