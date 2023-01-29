---
title: What is the syntax for creating a method that accepts a lambda as an argument in Java 8?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Define the method as taking a java.util.function.Consumer as a parameter.
---

**Contents**

[TOC]

### Defining the Method

To define a method which takes a lambda as a parameter in Java 8, use the following syntax:

```java
public void myMethod(MyLambdaInterface lambda) {
    // method body
}
```

Where `MyLambdaInterface` is an interface with a single abstract method that matches the signature of the lambda.

### Implementing the Method

To implement the method, use the following syntax:

```java
public void myMethod(MyLambdaInterface lambda) {
    // method body
    lambda.myLambdaMethod();
}
```

Where `myLambdaMethod()` is the method defined in the `MyLambdaInterface` interface.

### Invoking the Method

To invoke the method, use the following syntax:

```java
myMethod(() -> {
    // lambda body
});
```

Where the lambda body contains the code to be executed when `myMethod()` is invoked.

### Example

For example, the following code defines and invokes a method which takes a lambda as a parameter:

```java
public void myMethod(MyLambdaInterface lambda) {
    // method body
    lambda.myLambdaMethod();
}

public static void main(String[] args) {
    myMethod(() -> {
        System.out.println("Hello World!");
    });
}
```

When invoked, the method prints "Hello World!" to the console.
