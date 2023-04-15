---
title: What is the syntax for printing all the elements of a list in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a for loop to iterate through the List and print out each element.
---

**Contents**

[TOC]

### Using a For Loop

A for loop can be used to iterate through the elements of a list and print each element.

```java
List<String> list = new ArrayList<String>();
list.add("element 1");
list.add("element 2");
list.add("element 3");

for(String s : list){
    System.out.println(s);
}
```

### Using an Enhanced For Loop

An enhanced for loop can also be used to iterate through the elements of a list and print each element.

```java
List<String> list = new ArrayList<String>();
list.add("element 1");
list.add("element 2");
list.add("element 3");

for(String s : list){
    System.out.println(s);
}
```

### Using an Iterator

An iterator can be used to iterate through the elements of a list and print each element.

```java
List<String> list = new ArrayList<String>();
list.add("element 1");
list.add("element 2");
list.add("element 3");

Iterator<String> iter = list.iterator();
while(iter.hasNext()){
    System.out.println(iter.next());
}
```

### Using a ForEach Loop

A forEach loop can also be used to iterate through the elements of a list and print each element.

```java
List<String> list = new ArrayList<String>();
list.add("element 1");
list.add("element 2");
list.add("element 3");

list.forEach(s -> System.out.println(s));
```
