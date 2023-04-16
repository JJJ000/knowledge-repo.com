---
title: Replace an element in a Java arraylist at a specified index
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: ArrayList`s set() method can be used to replace an element at a specific index.
---

**Contents**

[TOC]

# Section 1: Introduction

Java ArrayList is a dynamic array implementation of the Java List interface. It is used to store and manipulate collections of data. It provides methods to manipulate the size of the array which is used internally to store the list.

# Section 2: Replace at Specific Index

The replace() method of the ArrayList class can be used to replace an element at a specified index in the list. This method takes two parameters: the index of the element to be replaced and the element to be stored at the specified index.

# Section 3: Example

The following example shows how to replace an element at a specific index in an ArrayList:

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
list.add("Orange");

// Replace "Banana" with "Mango"
list.set(1, "Mango");

System.out.println(list);
// Output: [Apple, Mango, Orange]
```

# Section 4: Conclusion

In this tutorial, we discussed how to replace an element at a specific index in an ArrayList. We also saw an example of how to use the replace() method to achieve this.
