---
title: Verify that an object is a particular type
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the instanceof operator to assert that an object is a specific type in Java.
---

**Contents**

[TOC]

1. Using the `instanceof` Operator 

The `instanceof` operator can be used to determine if an object is an instance of a particular class or interface. This operator returns true if the object is an instance of the specified class or interface, and false otherwise. 

Syntax:
```
object instanceof type
```

Example:
```
String str = "Hello World";
boolean result = str instanceof String;
System.out.println(result);
```

Output:
```
true
```

2. Using the `getClass()` Method 

The `getClass()` method is a method of the Object class and can be used to determine the class of an object. This method returns an object of type Class which contains information about the class of the object. 

Syntax:
```
object.getClass();
```

Example:
```
String str = "Hello World";
Class<?> cls = str.getClass();
System.out.println(cls.getName());
```

Output:
```
java.lang.String
```
