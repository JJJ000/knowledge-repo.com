---
title: What is the syntax for transforming a list of integers to an int array in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the .stream().mapToInt(IntegerintValue).toArray() method.
---

**Contents**

[TOC]

### Creating an int Array

One way to convert a List<Integer> to an int[] is to create an int array of the same size as the List<Integer>. This can be done with the following code:

```
int[] array = new int[list.size()];
```

### Populating the Array

Once the array is created, it can be populated with the elements from the List<Integer>. This can be done with a for loop:

```
for (int i = 0; i < list.size(); i++) {
    array[i] = list.get(i);
}
```

### Using Streams

Alternatively, the List<Integer> can be converted to an int[] using streams. This can be done with the following code:

```
int[] array = list.stream().mapToInt(i -> i).toArray();
```

### Using Guava

Finally, the List<Integer> can be converted to an int[] using the Google Guava library. This can be done with the following code:

```
int[] array = Ints.toArray(list);
```
