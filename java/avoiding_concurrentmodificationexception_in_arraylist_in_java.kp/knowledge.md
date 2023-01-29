---
title: What is the best way to remove elements from an "arraylist" while iterating without causing a "concurrentmodificationexception"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use an Iterator to iterate the ArrayList and call the Iterator`s remove() method to remove elements.
---

**Contents**

[TOC]

### Option 1: Iterator
The safest and most reliable way to avoid a `ConcurrentModificationException` when removing elements from an `ArrayList` while iterating is to use an `Iterator`. An `Iterator` allows you to traverse the list and remove elements without causing a `ConcurrentModificationException`.

### Example
```java
List<String> list = new ArrayList<String>();
list.add("A");
list.add("B");
list.add("C");

Iterator<String> it = list.iterator();
while (it.hasNext()) {
   String str = it.next();
   if (str.equals("B")) {
      it.remove();
   }
}
```

### Option 2: Copy the List
Another option is to make a copy of the `ArrayList` before iterating. This creates a snapshot of the list that can be iterated without causing a `ConcurrentModificationException`.

### Example
```java
List<String> list = new ArrayList<String>();
list.add("A");
list.add("B");
list.add("C");

List<String> copyList = new ArrayList<String>(list);
for (String str : copyList) {
   if (str.equals("B")) {
      list.remove(str);
   }
}
```

### Option 3: Use a While Loop
Another way to avoid a `ConcurrentModificationException` is to use a `while` loop instead of a `for` loop. This allows you to remove elements from the `ArrayList` without causing an exception.

### Example
```java
List<String> list = new ArrayList<String>();
list.add("A");
list.add("B");
list.add("C");

int i = 0;
while (i < list.size()) {
   String str = list.get(i);
   if (str.equals("B")) {
      list.remove(str);
   } else {
      i++;
   }
}
```

### Option 4: Use a ListIterator
The last option is to use a `ListIterator`. This allows you to traverse the list backwards and remove elements without causing a `ConcurrentModificationException`.

### Example
```java
List<String> list = new ArrayList<String>();
list.add("A");
list.add("B");
list.add("C");

ListIterator<String> it = list.listIterator(list.size());
while (it.hasPrevious()) {
   String str = it.previous();
   if (str.equals("B")) {
      it.remove();
   }
}
```
