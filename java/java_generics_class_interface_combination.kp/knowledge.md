---
title: Using Java generics with a class and an interface simultaneously
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A class and an interface can both be generic, meaning they can both use type parameters to accept multiple types of input.
---

**Contents**

[TOC]

### Class

Generics can be used with classes by declaring type parameters in the class definition. For example, a generic class definition might look like this:

```java
public class MyClass<T> {
    private T value;
    
    public MyClass(T value) {
        this.value = value;
    }
    
    public T getValue() {
        return value;
    }
}
```

This class has a type parameter T, which can be used to specify the type of the value field. For instance, if we wanted to create an instance of MyClass that stores a String, we could do so by specifying the type parameter as String:

```java
MyClass<String> myClass = new MyClass<>("Hello World!");
```

### Interface

Generics can also be used with interfaces. For example, a generic interface definition might look like this:

```java
public interface MyInterface<T> {
    public T getValue();
}
```

This interface has a type parameter T, which can be used to specify the type of the return value of the getValue() method. For instance, if we wanted to create an instance of MyInterface that returns a String, we could do so by specifying the type parameter as String:

```java
MyInterface<String> myInterface = () -> "Hello World!";
```
