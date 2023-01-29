---
title: What is the process for extracting a subset of elements from an array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Arrays.copyOfRange() method to create a subarray from another array in Java.
---

**Contents**

[TOC]

### Declaring an Array

An array can be declared in Java by specifying the data type of the elements followed by the name of the array and the size of the array within brackets. For example:

```java
int[] myArray = new int[5];
```

### Adding Elements to an Array

Elements can be added to an array by using the array index and assigning a value to it. For example:

```java
myArray[0] = 1;
myArray[1] = 2;
myArray[2] = 3;
myArray[3] = 4;
myArray[4] = 5;
```

### Creating a Sub Array

To create a sub array from an existing array, you can use the `Arrays.copyOfRange()` method. This method takes three parameters; the array to be copied, the starting index of the sub array and the ending index. For example:

```java
int[] subArray = Arrays.copyOfRange(myArray, 2, 4);
```

This will create a sub array containing the elements at index 2 and 3 of the original array.

### Verifying the Sub Array

To verify that the sub array was created correctly, you can use the `Arrays.toString()` method to print out the contents of the array. For example:

```java
System.out.println(Arrays.toString(subArray));
```

This will print out the contents of the sub array, which should be `[3, 4]`.
