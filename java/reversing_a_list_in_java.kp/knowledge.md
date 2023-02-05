---
title: Looping through a list in Java starting from the end
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To iterate through a list in reverse order in Java, use a for loop starting at the end of the list and decrementing the index.
---

**Contents**

[TOC]

**Section 1: Using a For Loop**

Using a for loop to iterate through a list in reverse order involves initializing a counter variable to the size of the list and then looping through the list from the end to the beginning. The counter variable should be decremented each time the loop runs.

```java
List<String> list = Arrays.asList("a", "b", "c");

for (int i = list.size() - 1; i >= 0; i--) {
    System.out.println(list.get(i));
}
```

**Section 2: Using a For-Each Loop**

Using a for-each loop to iterate through a list in reverse order involves looping through the list from the end to the beginning and using a decrementing iterator.

```java
List<String> list = Arrays.asList("a", "b", "c");

for (Iterator<String> iter = list.listIterator(list.size()); iter.hasPrevious(); ) {
    System.out.println(iter.previous());
}
```

**Section 3: Using a While Loop**

Using a while loop to iterate through a list in reverse order involves initializing a counter variable to the size of the list and then looping through the list from the end to the beginning. The counter variable should be decremented each time the loop runs.

```java
List<String> list = Arrays.asList("a", "b", "c");

int i = list.size() - 1;
while (i >= 0) {
    System.out.println(list.get(i));
    i--;
}
```

**Section 4: Using Java 8 Streams**

Using Java 8 Streams to iterate through a list in reverse order involves creating a stream from the list and then calling the `forEachOrdered` method with a lambda expression to loop through the list from the end to the beginning.

```java
List<String> list = Arrays.asList("a", "b", "c");

list.stream().forEachOrdered(s -> System.out.println(s));
```
