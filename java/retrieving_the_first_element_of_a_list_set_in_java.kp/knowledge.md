---
title: What is the method for accessing the first item in a list or set?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To get the first element of a List or Set in Java, use the iterator() or listIterator() method.
---

**Contents**

[TOC]

### Using for-loop

We can use a for-loop to iterate through the list or set and get the first element.

```java
List<String> list = new ArrayList<>();
list.add("one");
list.add("two");
list.add("three");

String firstElement = null;
for (String s : list) {
    firstElement = s;
    break;
}
```

### Using Iterator

We can also use an Iterator to get the first element of the list or set.

```java
List<String> list = new ArrayList<>();
list.add("one");
list.add("two");
list.add("three");

Iterator<String> iterator = list.iterator();
String firstElement = iterator.next();
```

### Using Stream

Using Stream API we can get the first element of the list or set.

```java
List<String> list = new ArrayList<>();
list.add("one");
list.add("two");
list.add("three");

String firstElement = list.stream().findFirst().orElse(null);
```

### Using List/Set Methods

We can also use List/Set methods to get the first element of the list or set.

```java
List<String> list = new ArrayList<>();
list.add("one");
list.add("two");
list.add("three");

String firstElement = list.get(0);
```
