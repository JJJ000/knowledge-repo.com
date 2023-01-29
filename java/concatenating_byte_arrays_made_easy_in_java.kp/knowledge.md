---
title: A simple method to join two byte arrays together
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Arrays.concat() method can be used to easily concatenate two byte arrays in Java.
---

**Contents**

[TOC]

### Option 1: Using Arrays.copyOf

The Arrays.copyOf method can be used to easily concatenate two byte arrays in Java. This method requires two parameters - the original byte array and the number of elements to be copied. The output of this method is a new byte array containing the elements of the original byte array plus the extra elements.

Syntax:

```
byte[] newArray = Arrays.copyOf(originalArray, newLength);
```

### Option 2: Using System.arraycopy

The System.arraycopy method can also be used to concatenate two byte arrays in Java. This method requires five parameters - the source array, the source starting index, the destination array, the destination starting index and the number of elements to be copied. The output of this method is a new byte array containing the elements of the source array plus the extra elements.

Syntax:

```
System.arraycopy(srcArray, srcPos, destArray, destPos, length);
```

### Option 3: Using Apache Commons Lang

The Apache Commons Lang library provides a utility method called ArrayUtils.addAll which can be used to concatenate two byte arrays in Java. This method requires two parameters - the original array and the array to be added. The output of this method is a new byte array containing the elements of both arrays.

Syntax:

```
byte[] newArray = ArrayUtils.addAll(originalArray, addedArray);
```

### Option 4: Using Java 8 Streams

Java 8 Streams can also be used to concatenate two byte arrays in Java. This method requires two parameters - the original array and the array to be added. The output of this method is a new byte array containing the elements of both arrays.

Syntax:

```
byte[] newArray = Stream.concat(Arrays.stream(originalArray), Arrays.stream(addedArray))
                        .toArray(byte[]::new);
```
