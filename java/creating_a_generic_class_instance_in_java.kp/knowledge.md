---
title: What is the process for creating an instance of a generic type t in a class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the class`s constructor to create an instance of type T.
---

**Contents**

[TOC]

`**` Create the Generic Class**

Create a generic class with the generic type parameter, T. This class will be used to create an instance of the generic type.

```java
public class GenericClass<T> {
    private T value;
    public GenericClass(T value) {
        this.value = value;
    }
    public T getValue() {
        return value;
    }
}
```

`**` Create the Instance**

Create an instance of the generic class using the generic type parameter.

```java
GenericClass<String> genericClass = new GenericClass<>("Hello World!");
```

`**` Retrieve the Instance**

Retrieve the instance of the generic type.

```java
String value = genericClass.getValue();
```

`**` Use the Instance**

Use the retrieved instance of the generic type.

```java
System.out.println(value); // prints "Hello World!"
```
