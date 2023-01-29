---
title: Duplicate an array
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To make a copy of an array in Java, use the Arrays.copyOf() method.
---

**Contents**

[TOC]

### Method 1: Using Arrays.copyOf()

The Arrays.copyOf() method can be used to create a shallow copy of an array. It takes two parameters, the original array and the size of the new array, which can be the same as or less than the size of the original array.

Syntax:

`public static <T> T[] copyOf(T[] original, int newLength)`

Example:

```java
int[] arr = {1, 2, 3};

int[] arrCopy = Arrays.copyOf(arr, arr.length);
```

### Method 2: Using System.arraycopy()

The System.arraycopy() method can be used to create a shallow copy of an array. It takes five parameters: the source array, the source index, the destination array, the destination index, and the length of the array to be copied.

Syntax:

`public static void arraycopy(Object src, int srcPos, Object dest, int destPos, int length)`

Example:

```java
int[] arr = {1, 2, 3};

int[] arrCopy = new int[arr.length];
System.arraycopy(arr, 0, arrCopy, 0, arr.length);
```

### Method 3: Using clone()

The clone() method can be used to create a shallow copy of an array. It takes no parameters and returns an Object, which must be cast to the appropriate array type.

Syntax:

`public Object clone()`

Example:

```java
int[] arr = {1, 2, 3};

int[] arrCopy = (int[]) arr.clone();
```

### Method 4: Using for loop

A for loop can be used to create a shallow copy of an array. It iterates through each element of the original array and copies them to the new array.

Syntax:

```java
int[] arr = {1, 2, 3};

int[] arrCopy = new int[arr.length];
for (int i = 0; i < arr.length; i++) {
    arrCopy[i] = arr[i];
}
```
