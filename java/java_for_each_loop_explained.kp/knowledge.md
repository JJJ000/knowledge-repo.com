---
title: What is the function of the Java `for each` loop?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Java `for each` loop iterates over a collection or array and executes a block of code for each element.
---

**Contents**

[TOC]

**Overview**
The Java `for each` loop is a type of loop that iterates over a collection of elements and executes a set of instructions for each element. It is a simplified version of the 'for' loop and is often used when the number of iterations is known.

**Syntax**
The syntax of the Java `for each` loop is as follows: 

```java
for (type item : collection) {
  // code block to be executed
}
```

Where 'type' is the type of the elements in the collection and 'item' is the name of the iterating variable.

**Example**
For example, if we have an array of integers and we want to print out each element of the array, we could use the Java `for each` loop as follows:

```java
int[] array = {1,2,3,4,5};
for (int item : array) {
  System.out.println(item);
}
```

This code will print out the following:
```java
1
2
3
4
5
```

**Conclusion**
The Java `for each` loop is a useful tool for iterating over collections of elements and performing a set of instructions for each element. It is a simplified version of the 'for' loop and can be used when the number of iterations is known.
