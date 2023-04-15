---
title: What is the syntax for creating a list<string> object in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A List<String> object can be initialized by using the List constructor, such as `List<String> list = new ArrayList<>();`.
---

**Contents**

[TOC]

### Create a List Object

A List object can be created using the `ArrayList<String>` constructor:

```java
List<String> list = new ArrayList<String>();
```

### Add Elements to the List

Elements can be added to the List using the `add()` method:

```java
list.add("Element 1");
list.add("Element 2");
list.add("Element 3");
```

### Access List Elements

Elements can be accessed using the `get()` method:

```java
String element1 = list.get(0); // element1 will be "Element 1"
String element2 = list.get(1); // element2 will be "Element 2"
String element3 = list.get(2); // element3 will be "Element 3"
```

### Iterate Over List Elements

The List can be iterated over using a `for` loop:

```java
for (int i = 0; i < list.size(); i++) {
    String element = list.get(i);
    System.out.println(element);
}
```
