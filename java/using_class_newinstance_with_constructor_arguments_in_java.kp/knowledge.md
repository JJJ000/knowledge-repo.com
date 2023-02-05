---
title: Is it possible to employ class.newinstance() with constructor arguments?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, Class.newInstance() cannot be used with constructor arguments in Java.
---

**Contents**

[TOC]

## Overview
The `Class.newInstance()` method is a Java reflection method used to create a new instance of a class. It is a convenient way to create objects without having to use the `new` keyword. It can also be used to create instances of inner classes.

## Using Constructor Arguments
The `Class.newInstance()` method can be used to create a new instance of a class with constructor arguments. To do this, the constructor must be declared `public` and the arguments must match the parameter types of the constructor. 

## Example
For example, consider the following class:

```java
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

The following code can be used to create an instance of `Person` with the constructor arguments `"John"` and `20`:

```java
Class<?> personClass = Person.class;
Object personObject = personClass.getConstructor(String.class, int.class).newInstance("John", 20);
Person person = (Person) personObject;
```

## Limitations
It is important to note that the `Class.newInstance()` method is not supported in all versions of Java. It is only supported in Java versions prior to Java 9. In Java 9 and later, the `Class.getDeclaredConstructor().newInstance()` method should be used instead.
