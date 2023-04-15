---
title: Invoking the remove method within a foreach loop in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can remove elements from a Collection while iterating over it using an Iterator`s remove() method.
---

**Contents**

[TOC]

### Solution

### Iteration with Iterator

The best way to remove elements from a collection while iterating is to use an Iterator. An Iterator is an interface that allows you to traverse through a collection of elements and remove elements from the collection. The following example demonstrates how to use an Iterator to remove elements from a List while iterating:

```java
List<String> list = new ArrayList<>();
list.add("A");
list.add("B");
list.add("C");

Iterator<String> iterator = list.iterator();
while(iterator.hasNext()) {
    String element = iterator.next();
    if (element.equals("B")) {
        iterator.remove();
    }
}
```

### Iteration with forEach

Java 8 introduced a new way to iterate through collections using the forEach() method. The forEach() method accepts a Consumer object which is a functional interface that can be used to perform an action on each element in the collection. The following example demonstrates how to use the forEach() method to remove elements from a List:

```java
List<String> list = new ArrayList<>();
list.add("A");
list.add("B");
list.add("C");

list.forEach(element -> {
    if (element.equals("B")) {
        list.remove(element);
    }
});
```

It should be noted that this approach is not thread-safe and can lead to ConcurrentModificationException if the list is modified by another thread while the forEach() loop is executing.

### Iteration with Stream API

Java 8 also introduced the Stream API which can be used to iterate through a collection and perform various operations. The following example demonstrates how to use the Stream API to remove elements from a List:

```java
List<String> list = new ArrayList<>();
list.add("A");
list.add("B");
list.add("C");

list = list.stream()
            .filter(element -> !element.equals("B"))
            .collect(Collectors.toList());
```

The Stream API is a powerful tool for iterating through collections and performing various operations. It is also thread-safe, so it can be used to safely iterate through collections in a multi-threaded environment.
