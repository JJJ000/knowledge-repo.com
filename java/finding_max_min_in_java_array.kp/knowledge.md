---
title: Determining the largest/smallest element in a collection of primitive data types using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the Arrays.stream().max() and Arrays.stream().min() methods to find the maximum and minimum values in an array of primitives.
---

**Contents**

[TOC]

**Section 1: Finding Max Value**

1. Create an array of primitives.

```java
int[] array = {2, 4, 6, 8, 10};
```

2. Declare an integer variable to store the maximum value.

```java
int maxValue = 0;
```

3. Iterate through the array and compare each element with the maximum value.

```java
for (int i = 0; i < array.length; i++) {
    if (array[i] > maxValue) {
        maxValue = array[i];
    }
}
```

4. Print out the maximum value.

```java
System.out.println("The maximum value is: " + maxValue);
```

**Section 2: Finding Min Value**

1. Create an array of primitives.

```java
int[] array = {2, 4, 6, 8, 10};
```

2. Declare an integer variable to store the minimum value.

```java
int minValue = array[0];
```

3. Iterate through the array and compare each element with the minimum value.

```java
for (int i = 0; i < array.length; i++) {
    if (array[i] < minValue) {
        minValue = array[i];
    }
}
```

4. Print out the minimum value.

```java
System.out.println("The minimum value is: " + minValue);
```
