---
title: Is there a quick way to set all elements in the array to zero?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, there is no one-line shortcut to initialize all array elements to zero in Java.
---

**Contents**

[TOC]

**Solution**

**Option 1: Using for loop**

```java
int[] array = new int[SIZE];
for (int i = 0; i < array.length; i++) {
    array[i] = 0;
}
```

**Option 2: Using Arrays.fill()**

```java
int[] array = new int[SIZE];
Arrays.fill(array, 0);
```

**Option 3: Using Arrays.stream()**

```java
int[] array = new int[SIZE];
Arrays.stream(array).forEach(i -> array[i] = 0);
```

**Option 4: Using Arrays.setAll()**

```java
int[] array = new int[SIZE];
Arrays.setAll(array, i -> 0);
```
