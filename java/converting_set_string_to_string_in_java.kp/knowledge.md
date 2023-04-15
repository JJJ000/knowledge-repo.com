---
title: What is the best way to turn a set of strings into a string array?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the toArray() method of the Set interface to convert a Set<String> to a String[].
---

**Contents**

[TOC]

### Solution 1: Using toArray() Method

The `toArray()` method of the `Set` interface can be used to convert a `Set` of type `String` to a `String` array. The syntax of the `toArray()` method is as follows:

```java
String[] myStringArray = myStringSet.toArray(new String[myStringSet.size()]);
```

Here, `myStringSet` is the `Set` of type `String` and `myStringArray` is the resultant `String` array.

### Solution 2: Using for-each Loop

A `for-each` loop can also be used to convert a `Set` of type `String` to a `String` array. The syntax of the `for-each` loop is as follows:

```java
String[] myStringArray = new String[myStringSet.size()];
int i = 0;
for(String s: myStringSet) {
    myStringArray[i] = s;
    i++;
}
```

Here, `myStringSet` is the `Set` of type `String` and `myStringArray` is the resultant `String` array.

### Solution 3: Using Iterator

An `Iterator` can also be used to convert a `Set` of type `String` to a `String` array. The syntax of the `Iterator` is as follows:

```java
String[] myStringArray = new String[myStringSet.size()];
Iterator<String> iterator = myStringSet.iterator();
int i = 0;
while(iterator.hasNext()) {
    myStringArray[i] = iterator.next();
    i++;
}
```

Here, `myStringSet` is the `Set` of type `String` and `myStringArray` is the resultant `String` array.

### Solution 4: Using Stream

The `Stream` API of Java 8 can also be used to convert a `Set` of type `String` to a `String` array. The syntax of the `Stream` API is as follows:

```java
String[] myStringArray = myStringSet.stream().toArray(String[]::new);
```

Here, `myStringSet` is the `Set` of type `String` and `myStringArray` is the resultant `String` array.
