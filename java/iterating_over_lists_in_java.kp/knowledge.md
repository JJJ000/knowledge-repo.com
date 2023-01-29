---
title: Iterating through a list in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: There are several ways to iterate over a list in Java, including using a for loop, enhanced for loop, while loop, and Iterator.
---

**Contents**

[TOC]

1. For Loop:
```java
for (int i = 0; i < list.size(); i++) {
    String item = list.get(i);
    // do something with item
}
```

2. For-Each Loop:
```java
for (String item : list) {
    // do something with item
}
```

3. Iterator:
```java
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    String item = iterator.next();
    // do something with item
}
```

4. ListIterator:
```java
ListIterator<String> listIterator = list.listIterator();
while (listIterator.hasNext()) {
    String item = listIterator.next();
    // do something with item
}
```
