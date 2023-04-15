---
title: What is the syntax for passing a function as a parameter in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, a function can be passed as a parameter by using a lambda expression or a method reference.
---

**Contents**

[TOC]

### Defining the Function

To pass a function as a parameter in Java, the function must first be defined. This is done by declaring a method with the desired parameters and return type. For example, the following function takes two integers as parameters and returns their sum:

```java
public int add(int x, int y) {
    return x + y;
}
```

### Declaring the Parameter

The next step is to declare the parameter type as a functional interface. A functional interface is an interface that has a single abstract method. In this case, the functional interface must match the signature of the function, i.e. it must have the same parameters and return type.

In Java 8, the `java.util.function` package contains several functional interfaces that can be used for this purpose. For example, the `BiFunction` interface is used to represent a function that takes two parameters and returns a result. The following code declares a `BiFunction` parameter:

```java
public void doSomething(BiFunction<Integer, Integer, Integer> func) {
    // ...
}
```

### Passing the Function

Finally, the function can be passed as an argument when calling the method. This is done by using a lambda expression, which is an anonymous function that can be used to pass a function as an argument. For example, the following code passes the `add` function as an argument to the `doSomething` method:

```java
doSomething((x, y) -> add(x, y));
```

### Using the Function

Once the function has been passed as a parameter, it can be used inside the method. For example, the following code uses the `func` parameter to calculate the sum of two integers:

```java
public void doSomething(BiFunction<Integer, Integer, Integer> func) {
    int result = func.apply(1, 2);
    // ...
}
```
