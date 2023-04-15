---
title: What is the syntax for combining two lists in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can join two lists in Java by using the addAll() method on one of the lists.
---

**Contents**

[TOC]

`**` Using Java 8 Streams**

The simplest way to join two lists in Java 8 is to use the Streams API. The Streams API provides a method called `concat()` which takes two `Stream`s and returns a single `Stream` containing all the elements of the two streams. This can be used to join two lists as follows:

```
List<String> list1 = Arrays.asList("a", "b", "c");
List<String> list2 = Arrays.asList("d", "e", "f");

List<String> joinedList = Stream.concat(list1.stream(), list2.stream())
                               .collect(Collectors.toList());
```

`**` Using Java 7 Loops**

If you are using Java 7 or earlier, you can join two lists by using a loop to iterate over the elements of one list and add them to the other. For example:

```
List<String> list1 = Arrays.asList("a", "b", "c");
List<String> list2 = Arrays.asList("d", "e", "f");

List<String> joinedList = new ArrayList<>();

for (String s : list1) {
    joinedList.add(s);
}

for (String s : list2) {
    joinedList.add(s);
}
```

`**` Using Apache Commons Lang**

If you are using Apache Commons Lang, you can use the `CollectionUtils.union()` method to join two lists. For example:

```
List<String> list1 = Arrays.asList("a", "b", "c");
List<String> list2 = Arrays.asList("d", "e", "f");

List<String> joinedList = CollectionUtils.union(list1, list2);
```

`**` Using Guava**

If you are using Guava, you can use the `Lists.newArrayList()` method to join two lists. For example:

```
List<String> list1 = Arrays.asList("a", "b", "c");
List<String> list2 = Arrays.asList("d", "e", "f");

List<String> joinedList = Lists.newArrayList(Iterables.concat(list1, list2));
```
