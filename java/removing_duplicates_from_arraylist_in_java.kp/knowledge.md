---
title: What is the best way to eliminate duplicate elements from an arraylist?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the removeIf() method to remove repeated elements from an ArrayList in Java.
---

**Contents**

[TOC]

### Using Java 8 Streams

Java 8 Streams provide a powerful way to filter and remove repeated elements from an ArrayList. The following code snippet shows how to remove duplicate elements from an ArrayList using streams:

```java
ArrayList<Integer> list = new ArrayList<>(Arrays.asList(1,2,2,3,3,4));
 
list = list.stream()
           .distinct()
           .collect(Collectors.toCollection(ArrayList::new));
```

### Using HashSet

HashSet is a collection that stores unique elements. It can be used to remove duplicate elements from an ArrayList. The following code snippet shows how to remove duplicate elements from an ArrayList using a HashSet:

```java
ArrayList<Integer> list = new ArrayList<>(Arrays.asList(1,2,2,3,3,4));

HashSet<Integer> set = new HashSet<>(list);
list.clear();
list.addAll(set);
```

### Using Iterator

Iterator can also be used to remove duplicate elements from an ArrayList. The following code snippet shows how to remove duplicate elements from an ArrayList using an Iterator:

```java
ArrayList<Integer> list = new ArrayList<>(Arrays.asList(1,2,2,3,3,4));

Iterator<Integer> itr = list.iterator();
while(itr.hasNext()){
    Integer element = itr.next();
    if(list.indexOf(element) != list.lastIndexOf(element)){
        itr.remove();
    }
}
```

### Using For Loop

A for loop can also be used to remove duplicate elements from an ArrayList. The following code snippet shows how to remove duplicate elements from an ArrayList using a for loop:

```java
ArrayList<Integer> list = new ArrayList<>(Arrays.asList(1,2,2,3,3,4));

for(int i = 0; i < list.size(); i++){
    for(int j = i+1; j < list.size(); j++){
        if(list.get(i).equals(list.get(j))){
            list.remove(j);
        }
    }
}
```
