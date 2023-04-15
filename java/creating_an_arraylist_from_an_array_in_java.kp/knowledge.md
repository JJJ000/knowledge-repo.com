---
title: How to construct an arraylist from an array in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can create an ArrayList from an array by using the constructor that takes an array as an argument.
---

**Contents**

[TOC]

### Step 1: Create an Array

Create an array of any type of elements:

```java
String[] array = {"Element1", "Element2", "Element3"};
```

### Step 2: Create an ArrayList

Create an ArrayList object, passing the array as a parameter:

```java
ArrayList<String> arrayList = new ArrayList<>(Arrays.asList(array));
```

### Step 3: Add Elements to the ArrayList

Add additional elements to the ArrayList:

```java
arrayList.add("Element4");
arrayList.add("Element5");
```

### Step 4: Retrieve Elements from the ArrayList

Retrieve elements from the ArrayList:

```java
String element = arrayList.get(0); // element will be "Element1"
```
