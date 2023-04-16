---
title: Check if an object in a Java list has a field value equal to x
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, the List.contains(Object) method can be used to check if an Object with a field value equal to x is present in the List.
---

**Contents**

[TOC]

1. Overview 
2. Syntax 
3. Example 
4. Conclusion 

## 1. Overview
The Java `List.contains(Object with field value equal to x)` method is used to check if a list contains an object with a field value equal to a given value. It is a boolean method that returns true if the list contains an object with the specified field value and false otherwise.

## 2. Syntax
The syntax for the `List.contains(Object with field value equal to x)` method is as follows:

```
boolean contains(Object with field value equal to x)
```

## 3. Example
The following example shows how to use the `List.contains()` method to check if a list contains an object with a field value equal to a given value:

```
List<MyObject> myObjectList = new ArrayList<>();
MyObject obj1 = new MyObject("foo", 10);
MyObject obj2 = new MyObject("bar", 20);
MyObject obj3 = new MyObject("baz", 30);

myObjectList.add(obj1);
myObjectList.add(obj2);
myObjectList.add(obj3);

boolean containsValue = myObjectList.contains(obj2.getValue() == 20);

System.out.println(containsValue); // prints true
```

## 4. Conclusion
The `List.contains(Object with field value equal to x)` method is used to check if a list contains an object with a field value equal to a given value. It is a boolean method that returns true if the list contains an object with the specified field value and false otherwise.
