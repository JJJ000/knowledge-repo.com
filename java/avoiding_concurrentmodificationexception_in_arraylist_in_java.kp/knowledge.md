---
title: To avoid a java.util.concurrentmodificationexception when iterating through and removing elements from an arraylist, use an iterator to loop through the list and call the iterator's remove() method to remove the elements
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use an Iterator to iterate through the ArrayList and call Iterator.remove() to remove elements.
---

**Contents**

[TOC]

# Option 1: Using Iterator

The Iterator interface provides a safe way to traverse a collection and modify it by removing elements. The `remove()` method of the iterator can be used to remove the current element from the collection.

```java
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    String element = iterator.next();
    if (element.equals("elementToRemove")) {
        iterator.remove();
    }
}
```

# Option 2: Using ListIterator

The ListIterator interface provides a safe way to traverse a list and modify it by removing elements. The `remove()` method of the list iterator can be used to remove the last element returned by the `next()` or `previous()` methods.

```java
ListIterator<String> iterator = list.listIterator();
while (iterator.hasNext()) {
    String element = iterator.next();
    if (element.equals("elementToRemove")) {
        iterator.remove();
    }
}
```

# Option 3: Using Copy

It is possible to avoid a ConcurrentModificationException by making a copy of the list before iterating over it. The copy can be modified without affecting the original list.

```java
List<String> copy = new ArrayList<>(list);
for (String element : copy) {
    if (element.equals("elementToRemove")) {
        list.remove(element);
    }
}
```

# Option 4: Using for-loop

It is possible to avoid a ConcurrentModificationException by using a for-loop with an explicit index. The index can be used to remove elements from the list.

```java
for (int i = 0; i < list.size(); i++) {
    String element = list.get(i);
    if (element.equals("elementToRemove")) {
        list.remove(i);
    }
}
```
