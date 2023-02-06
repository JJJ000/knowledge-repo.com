---
title: How to add elements to the beginning of a Java arraylist
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the add(int index, E element) method to add elements at the beginning of an ArrayList.
---

**Contents**

[TOC]

# Adding Elements at the Beginning of an ArrayList

## Using add() Method
The `add()` method of the ArrayList class can be used to add elements at the beginning of the list. 

Syntax:
```
public void add(int index, E element)
```

Example:
```
ArrayList<String> list = new ArrayList<String>();
list.add(0, "Apple");
list.add(0, "Mango");
```

## Using addAll() Method
The `addAll()` method of the ArrayList class can be used to add all elements of a collection at the beginning of the list.

Syntax:
```
public boolean addAll(int index, Collection<? extends E> c)
```

Example:
```
ArrayList<String> list = new ArrayList<String>();
List<String> fruits = Arrays.asList("Apple", "Mango");
list.addAll(0, fruits);
```

## Using LinkedList
The `LinkedList` class can be used to add elements at the beginning of the list. The `addFirst()` method of the LinkedList class can be used to add an element at the beginning of the list.

Syntax:
```
public void addFirst(E e)
```

Example:
```
LinkedList<String> list = new LinkedList<String>();
list.addFirst("Apple");
list.addFirst("Mango");
```
