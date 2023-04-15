---
title: What is the process for accessing the value of a private field from a different class in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Private fields cannot be accessed directly from a different class in Java, so a public getter method must be used to read the value.
---

**Contents**

[TOC]

### Reflection 
Reflection is a feature in the Java programming language that allows code to inspect and manipulate the fields, methods, and constructors of loaded classes at run time. Reflection can be used to read the value of a private field from a different class in Java. 

### Steps 
1. Get the Class object of the target class using `Class.forName()` method. 
2. Get the desired Field object from the Class object using `getDeclaredField()` method.
3. Set the `accessible` property of the Field object to `true` using `setAccessible()` method.
4. Get the value of the Field object using `get()` method.

### Example

```java
public class Main {
    public static void main(String[] args) {
        try {
            Class<?> targetClass = Class.forName("TargetClass");
            Field privateField = targetClass.getDeclaredField("privateField");
            privateField.setAccessible(true);
            Object value = privateField.get(null);
            System.out.println(value);
        } catch (ClassNotFoundException | NoSuchFieldException | IllegalAccessException e) {
            e.printStackTrace();
        }
    }
}
```
