---
title: What is the process for changing an int array into a list of integers in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Arrays.stream(int[]) method to convert the int[] array into a Stream<Integer>, then use the Stream.collect(Collectors.toList()) method to collect the stream into a List<Integer>.
---

**Contents**

[TOC]

### Using Streams

The easiest way to convert an int[] array into a List<Integer> is by using the Streams API. 

The following code snippet shows how to do this:

```
int[] array = {1,2,3,4,5};
List<Integer> list = Arrays.stream(array).boxed().collect(Collectors.toList());
```

### Using For Loop

We can also use a for loop to convert an int[] array into a List<Integer>.

The following code snippet shows how to do this:

```
int[] array = {1,2,3,4,5};
List<Integer> list = new ArrayList<>();
for(int i : array){
    list.add(i);
}
```

### Using List Constructor

We can also use the List constructor to convert an int[] array into a List<Integer>.

The following code snippet shows how to do this:

```
int[] array = {1,2,3,4,5};
List<Integer> list = new ArrayList<>(Arrays.asList(array));
```

### Using Apache Commons Library

We can also use the Apache Commons library to convert an int[] array into a List<Integer>.

The following code snippet shows how to do this:

```
int[] array = {1,2,3,4,5};
List<Integer> list = new ArrayList<>(Ints.asList(array));
```
