---
title: What is the syntax for passing an arraylist to a varargs method parameter?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pass the ArrayList as an argument to the varargs method, preceded by the spread operator (three dots `...`).
---

**Contents**

[TOC]

### Creating the ArrayList

The first step in passing an `ArrayList` to a varargs method parameter is to create the `ArrayList` itself. This can be done using the `ArrayList` constructor and passing the desired type as a parameter.

```java
ArrayList<Integer> list = new ArrayList<>();
```

### Adding Elements

Once the `ArrayList` is created, elements can be added to it using the `add` method.

```java
list.add(1);
list.add(2);
list.add(3);
```

### Converting to an Array

To pass the `ArrayList` to a varargs method parameter, it must be converted to an array. This can be done using the `toArray` method.

```java
Integer[] arr = list.toArray(new Integer[list.size()]);
```

### Passing to the Method

Finally, the array can be passed to the varargs method.

```java
myMethod(arr);
```
