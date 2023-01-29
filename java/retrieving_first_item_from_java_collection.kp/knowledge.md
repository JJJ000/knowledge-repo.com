---
title: Retrieve the first element from a Java collection
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The first item in a collection can be retrieved using the collection`s iterator`s next() method.
---

**Contents**

[TOC]

### Using for-each loop

```java
Collection<Item> items = ...
Item firstItem = null;

for (Item item : items) {
    firstItem = item;
    break;
}
```

### Using Iterator

```java
Collection<Item> items = ...
Item firstItem = null;

Iterator<Item> iterator = items.iterator();
if (iterator.hasNext()) {
    firstItem = iterator.next();
}
```

### Using Stream

```java
Collection<Item> items = ...
Item firstItem = items.stream().findFirst().orElse(null);
```

### Using List

```java
List<Item> items = ...
Item firstItem = items.get(0);
```
