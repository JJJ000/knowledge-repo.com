---
title: Retrieving the class name using a static method in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The class name can be retrieved using the getClass() method on the class object.
---

**Contents**

[TOC]

### Using Reflection

The `Class` class provides a static method called `forName()` which can be used to get the class name from a static method in Java. This method takes a `String` argument representing the fully qualified name of the desired class. The following example demonstrates how to use `forName()` to get the class name from a static method:

```java
String className = MyStaticClass.class.getName();
Class<?> clazz = Class.forName(className);
```

### Using `getClass()` Method

The `Class` class also provides a non-static method called `getClass()` which can be used to get the class name from a static method in Java. This method returns an instance of the `Class` class for the object on which it is called. The following example demonstrates how to use `getClass()` to get the class name from a static method:

```java
Class<?> clazz = MyStaticClass.getClass();
```

### Using `getSimpleName()` Method

The `Class` class also provides a non-static method called `getSimpleName()` which can be used to get the simple name of the class from a static method in Java. This method returns a `String` representing the simple name of the class. The following example demonstrates how to use `getSimpleName()` to get the class name from a static method:

```java
String className = MyStaticClass.getClass().getSimpleName();
```

### Using `getCanonicalName()` Method

The `Class` class also provides a non-static method called `getCanonicalName()` which can be used to get the canonical name of the class from a static method in Java. This method returns a `String` representing the canonical name of the class. The following example demonstrates how to use `getCanonicalName()` to get the class name from a static method:

```java
String className = MyStaticClass.getClass().getCanonicalName();
```
