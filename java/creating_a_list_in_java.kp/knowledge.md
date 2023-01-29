---
title: What is the syntax for creating a list in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To make a new List in Java, use the List interface and its implementations such as ArrayList, LinkedList, etc.
---

**Contents**

[TOC]

### Create an ArrayList

The first step to creating a new List in Java is to create an ArrayList. An ArrayList is a type of List that stores its elements in an array, which is a collection of objects of the same type. To create an ArrayList, use the following syntax:

```java
ArrayList<Type> listName = new ArrayList<>();
```

Replace `Type` with the type of elements the List will store and `listName` with the name of the List.

### Add Elements to the List

Once the List has been created, elements can be added to it using the `add()` method. The `add()` method takes one argument, which is the element to be added to the List. The syntax for adding an element to the List is as follows:

```java
listName.add(element);
```

Replace `listName` with the name of the List and `element` with the element to be added.

### Access Elements in the List

Once elements have been added to the List, they can be accessed using the `get()` method. The `get()` method takes one argument, which is the index of the element to be accessed. The syntax for accessing an element in the List is as follows:

```java
listName.get(index);
```

Replace `listName` with the name of the List and `index` with the index of the element to be accessed.

### Iterate Through the List

The elements in the List can also be iterated through using a for loop. The syntax for iterating through the List is as follows:

```java
for (Type element : listName) {
    // Do something with the element
}
```

Replace `Type` with the type of elements the List contains and `listName` with the name of the List.
