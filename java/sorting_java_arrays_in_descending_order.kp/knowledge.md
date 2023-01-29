---
title: How can I sort a Java array in descending order?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To sort an array in descending order, use the Arrays.sort() method with the Collections.reverseOrder() comparator.
---

**Contents**

[TOC]

### Sort Descending

### Step 1: Create Array
Create an array of elements to be sorted.

```java
int[] array = {2, 5, -2, 6, -3, 8, 0, -7, -9, 4};
```

### Step 2: Use Arrays.sort()
Use the Arrays.sort() method to sort the array in descending order.

```java
Arrays.sort(array);
```

### Step 3: Reverse Array
Reverse the array to sort it in descending order.

```java
for (int i = 0; i < array.length / 2; i++) {
    int temp = array[i];
    array[i] = array[array.length - i - 1];
    array[array.length - i - 1] = temp;
}
```

### Step 4: Print Array
Print the sorted array.

```java
System.out.println(Arrays.toString(array));
```

Output:
```
[8, 6, 5, 4, 2, 0, -2, -3, -7, -9]
```
