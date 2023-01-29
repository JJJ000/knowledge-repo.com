---
title: What is the best way to loop through a set/hashset without an iterator?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can iterate over a Set/HashSet without an Iterator in Java by using a for-each loop.
---

**Contents**

[TOC]

1. Using a For-Each Loop

Java provides a for-each loop which can iterate over a set without using an iterator. This loop is useful when we need to iterate over a set and perform some operation on its elements.

The syntax of the for-each loop is:

```
for(Element e : Set) {
  // code to be executed
}
```

For example, let's say we want to print all the elements of a set:

```
Set<Integer> mySet = new HashSet<>();
mySet.add(1);
mySet.add(2);
mySet.add(3);

for(Integer element : mySet) {
  System.out.println(element);
}
```

2. Using a Lambda Expression

Java 8 introduced the concept of lambda expressions which allow us to iterate over a set without using an iterator. Lambda expressions are useful when we need to perform some operation on each element of the set.

The syntax of the lambda expression is:

```
Set.forEach(element -> {
  // code to be executed
});
```

For example, let's say we want to print all the elements of a set:

```
Set<Integer> mySet = new HashSet<>();
mySet.add(1);
mySet.add(2);
mySet.add(3);

mySet.forEach(element -> {
  System.out.println(element);
});
```

3. Using a Stream

Java 8 introduced the concept of streams which allow us to iterate over a set without using an iterator. Streams are useful when we need to perform some operation on each element of the set.

The syntax of the stream is:

```
Set.stream().forEach(element -> {
  // code to be executed
});
```

For example, let's say we want to print all the elements of a set:

```
Set<Integer> mySet = new HashSet<>();
mySet.add(1);
mySet.add(2);
mySet.add(3);

mySet.stream().forEach(element -> {
  System.out.println(element);
});
```

4. Using a List

We can also iterate over a set without using an iterator by first converting it to a list and then iterating over the list. This is useful when we need to perform some operation on each element of the set.

The syntax of the list iteration is:

```
List<Element> myList = new ArrayList<>(Set);
for(Element e : myList) {
  // code to be executed
}
```

For example, let's say we want to print all the elements of a set:

```
Set<Integer> mySet = new HashSet<>();
mySet.add(1);
mySet.add(2);
mySet.add(3);

List<Integer> myList = new ArrayList<>(mySet);
for(Integer element : myList) {
  System.out.println(element);
}
```
