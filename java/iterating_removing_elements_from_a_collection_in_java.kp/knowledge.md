---
title: Iterate through a collection while taking out elements
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not recommended to remove elements from a collection while iterating over it in Java.
---

**Contents**

[TOC]

### Iterating with Iterator

The easiest way to remove elements from a collection while iterating is to use an Iterator. An Iterator is an object that can be used to traverse through a collection and access its elements. The Iterator provides a method called `remove()` which can be used to remove the current element from the collection.

Example:

```java
Iterator<String> iterator = collection.iterator();
while (iterator.hasNext()) {
    String element = iterator.next();
    if (element.equals("some element")) {
        iterator.remove();
    }
}
```

### Iterating with for-each Loop

It is also possible to remove elements from a collection while iterating using a for-each loop. This can be done by creating a temporary collection and adding all the elements to it, except for the ones that need to be removed. The temporary collection can then be used to update the original collection.

Example:

```java
List<String> tempList = new ArrayList<>();
for (String element : collection) {
    if (!element.equals("some element")) {
        tempList.add(element);
    }
}
collection.clear();
collection.addAll(tempList);
```

### Iterating with ListIterator

Another way to remove elements from a collection while iterating is to use a ListIterator. A ListIterator is an object that can be used to traverse through a list and access its elements. The ListIterator provides a method called `remove()` which can be used to remove the current element from the list.

Example:

```java
ListIterator<String> listIterator = list.listIterator();
while (listIterator.hasNext()) {
    String element = listIterator.next();
    if (element.equals("some element")) {
        listIterator.remove();
    }
}
```
