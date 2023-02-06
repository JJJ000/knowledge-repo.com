---
title: What is the syntax for creating an arraylist containing values?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: An ArrayList can be declared with values in Java by using the syntax `ArrayList<Type> arrayListName = new ArrayList<Type>(Arrays.asList(values));`.
---

**Contents**

[TOC]

### 1. Declaring an ArrayList

An ArrayList can be declared in Java using the following syntax:

```java
ArrayList<Type> arrayListName = new ArrayList<Type>();
```

Where `Type` is the type of values that the ArrayList will hold and `arrayListName` is the name of the ArrayList.

### 2. Adding Values to the ArrayList

Values can be added to the ArrayList using the `add()` method. This method takes a single argument which is the value to be added to the ArrayList.

For example, to add an integer value to an ArrayList of type `Integer`:

```java
arrayListName.add(10);
```

### 3. Declaring an ArrayList with Values

To declare an ArrayList with values, the `ArrayList` constructor can be used. This constructor takes a `Collection` as an argument and adds all elements of the `Collection` to the ArrayList.

For example, to declare an ArrayList of type `Integer` with the values `10`, `20` and `30`:

```java
ArrayList<Integer> arrayListName = new ArrayList<Integer>(Arrays.asList(10, 20, 30));
```

### 4. Iterating Through the ArrayList

The elements of the ArrayList can be accessed and iterated through using the `for-each` loop.

For example, to iterate through the ArrayList declared in the previous section:

```java
for (Integer value : arrayListName) {
    System.out.println(value);
}
```

The above code will print the values `10`, `20` and `30` to the console.
