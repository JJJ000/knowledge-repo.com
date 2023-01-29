---
title: What is the process for creating a hashset with values using a constructor?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can initialize a HashSet with a collection of values by passing the collection to the HashSet constructor.
---

**Contents**

[TOC]

`**` Create a HashSet Object**

The first step in initializing HashSet values by construction is to create a HashSet object. This can be done using the following syntax:

`HashSet<Type> hs = new HashSet<Type>();`

Where `Type` is the type of elements that will be stored in the HashSet.

`**` Add Elements to the HashSet**

Once the HashSet object has been created, elements can be added to it using the `add()` method. This can be done using the following syntax:

`hs.add(element);`

Where `element` is the element that is to be added to the HashSet.

`**` Initialize the HashSet with a Collection**

It is also possible to initialize the HashSet with a collection of elements. This can be done using the `addAll()` method. This can be done using the following syntax:

`hs.addAll(collection);`

Where `collection` is the collection of elements that is to be added to the HashSet.

`**` Initialize the HashSet with an Array**

Finally, it is also possible to initialize the HashSet with an array of elements. This can be done using the `addAll()` method. This can be done using the following syntax:

`hs.addAll(array);`

Where `array` is the array of elements that is to be added to the HashSet.
