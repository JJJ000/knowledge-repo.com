---
title: What is the process for transforming a collection into a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The collection can be converted to a List by using the Collection.toArray() method and passing the result to the Arrays.asList() method.
---

**Contents**

[TOC]

### Overview
A Collection is an interface in the Java Collection Framework that represents a group of objects, known as its elements. A List is an ordered collection (sometimes called a sequence). It allows positional access to its elements and provides a way to insert and remove elements.

### Steps
1. Create a List object.
2. Use the addAll() method of the List interface to add the elements of the Collection to the List.
3. Use the toArray() method of the Collection interface to get an array of the elements in the Collection.
4. Use the addAll() method of the List interface to add the elements of the array to the List.

### Example
The following example shows how to convert a Collection to a List:

```java
// Create a Collection 
Collection<String> collection = new ArrayList<String>(); 
collection.add("John"); 
collection.add("Bob"); 
collection.add("Steve"); 

// Create a List 
List<String> list = new ArrayList<String>(); 

// Add the elements of the Collection to the List 
list.addAll(collection); 

// Get an array of the elements in the Collection 
Object[] array = collection.toArray(); 

// Add the elements of the array to the List 
list.addAll(Arrays.asList(array));
```

### Conclusion
In this tutorial, we learned how to convert a Collection to a List in Java. We used the addAll() method of the List interface to add the elements of the Collection to the List, and the toArray() method of the Collection interface to get an array of the elements in the Collection. Finally, we used the addAll() method of the List interface to add the elements of the array to the List.
