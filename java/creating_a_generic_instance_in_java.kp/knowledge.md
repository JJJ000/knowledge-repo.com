---
title: How do you instantiate a generic type in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can create an instance of a generic type in Java by using the syntax `ClassName<Type> objectName = new ClassName<Type>();`.
---

**Contents**

[TOC]

### Step 1: Create the Class

Create a generic class with the type parameter. For example:

```java
public class MyGenericClass<T> {
  // Class code here
}
```

### Step 2: Instantiate the Class

Instantiate the generic class with the type parameter. For example:

```java
MyGenericClass<String> myGenericClass = new MyGenericClass<>();
```

### Step 3: Use the Instance

Use the instance of the generic class. For example:

```java
myGenericClass.someMethod();
```
