---
title: What is the class of an object?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The class of an object in Java can be determined using the getClass() method.
---

**Contents**

[TOC]

1. Using the `getClass()` Method
--------------------------------
The `getClass()` method is a method of the `Object` class which is inherited by all other classes. It returns the `Class` object associated with the object.

Example:
```java
Object obj = new Object();
Class cls = obj.getClass();
System.out.println("Class of Object obj is: " + cls.getName());
```

Output:
```
Class of Object obj is: java.lang.Object
```

2. Using the `instanceof` Operator
---------------------------------
The `instanceof` operator is used to determine whether an object is an instance of a particular class or interface.

Example:
```java
Object obj = new String("Hello World");
if (obj instanceof String) {
    System.out.println("obj is an instance of String");
}
```

Output:
```
obj is an instance of String
```

3. Using the `Class.forName()` Method
------------------------------------
The `Class.forName()` method is used to get the `Class` object associated with a class name.

Example:
```java
Class cls = Class.forName("java.lang.String");
System.out.println("Class of String is: " + cls.getName());
```

Output:
```
Class of String is: java.lang.String
```

4. Using Reflection
-------------------
Reflection is a way to examine and modify the runtime behavior of a class. It allows us to inspect the class, interface, fields and methods at runtime, without knowing the names of the classes, methods etc. at compile time.

Example:
```java
Object obj = new String("Hello World");
Class cls = obj.getClass();
System.out.println("Class of Object obj is: " + cls.getName());
```

Output:
```
Class of Object obj is: java.lang.String
```
