---
title: What is the type parameter of java.util.list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The generic type of java.util.List is `E`.
---

**Contents**

[TOC]

1. Overview 
2. Syntax 
3. Examples 

### 1. Overview 
The generic type of java.util.List is a parameterized type, which is a type that is created by combining a generic type with specific types of its parameters. It is used to create a type-safe collection that can hold only a certain type of objects. 

### 2. Syntax 
The syntax for creating a generic type of java.util.List is as follows: 
```java
List<Type> listName = new ArrayList<Type>();
```
where Type is the type of objects that the list will hold. 

### 3. Examples 
Here are some examples of creating a generic type of java.util.List: 
```java
List<String> stringList = new ArrayList<String>();
List<Integer> intList = new ArrayList<Integer>();
List<Person> personList = new ArrayList<Person>();
```
