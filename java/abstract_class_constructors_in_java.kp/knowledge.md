---
title: Is it possible for an abstract class to have a constructor?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, an abstract class can have a constructor in Java.
---

**Contents**

[TOC]

### Yes
An abstract class can have a constructor in Java. Constructors are used to initialize the state of an object, and abstract classes are no exception.

### Why
Constructors in abstract classes are used to initialize the state of the class, such as setting up any static fields or initializing any variables that need to be initialized before the class is used.

### How
To create a constructor in an abstract class, the constructor must be declared with the same access modifier as the abstract class. For example, if the abstract class is declared as public, then the constructor must also be declared as public.

### Example

```java
public abstract class Animal {
    private int age;
    
    public Animal(int age) {
        this.age = age;
    }
    
    public int getAge() {
        return age;
    }
}
```
