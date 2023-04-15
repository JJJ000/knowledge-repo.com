---
title: What is the syntax for combining two arrays in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `ArrayUtils.addAll()` method from Apache Commons Lang to concatenate two arrays in Java.
---

**Contents**

[TOC]

### Using the System Class

The easiest way to concatenate two arrays in Java is to use the `System.arraycopy()` method. This method takes three parameters: the source array, the destination array, and the number of elements to copy. It copies the elements from the source array to the destination array starting at the specified index.

To concatenate two arrays, create a new array with the desired length, and then use `System.arraycopy()` to copy the elements from each of the source arrays into the new array.

### Using the Arrays Class

The `java.util.Arrays` class provides a static `concat()` method for concatenating two arrays. It takes two arrays as arguments and returns a new array containing the elements from both of the input arrays.

### Using the ArrayList Class

The `java.util.ArrayList` class provides a `addAll()` method for concatenating two arrays. It takes two arrays as arguments and adds all of the elements from the first array to the end of the second array.

### Using the Stream API

The `java.util.stream.Stream` class provides a `concat()` method for concatenating two arrays. It takes two arrays as arguments and returns a new `Stream` containing the elements from both of the input arrays. The resulting `Stream` can then be converted to an array using the `toArray()` method.
