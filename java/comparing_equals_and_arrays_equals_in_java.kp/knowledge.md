---
title: Comparing two objects with 'equals' versus comparing two arrays with 'arrays.equals' in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Arrays.equals compares two arrays to see if they contain the same elements in the same order, while the == operator simply checks if the two arrays are the same object.
---

**Contents**

[TOC]

##### Difference
`equals()` is a method defined in the Object class. It compares two object references to check if they refer to the same object. `Arrays.equals()` is a method defined in the Arrays class. It compares two arrays to check if they contain the same elements in the same order.

##### When to Use
`equals()` should be used when comparing two object references to check if they refer to the same object. `Arrays.equals()` should be used when comparing two arrays to check if they contain the same elements in the same order.

##### Example
```
Object obj1 = new Object();
Object obj2 = new Object();

if (obj1.equals(obj2)) {
    System.out.println("Objects are equal");
} else {
    System.out.println("Objects are not equal");
}

int[] arr1 = {1, 2, 3};
int[] arr2 = {1, 2, 3};

if (Arrays.equals(arr1, arr2)) {
    System.out.println("Arrays are equal");
} else {
    System.out.println("Arrays are not equal");
}
```

##### Output
Objects are not equal
Arrays are equal
