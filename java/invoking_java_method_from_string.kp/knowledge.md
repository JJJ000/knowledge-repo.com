---
title: What is the syntax for calling a Java method when the name of the method is stored in a string variable?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the reflection API to invoke a Java method when given the method name as a string.
---

**Contents**

[TOC]

### Reflection API

The Java Reflection API provides a way to invoke a Java method when given the method name as a string. This is done by using the `Class.getDeclaredMethod()` method, which takes a string representing the method name as an argument. 

To invoke the method, the `Method.invoke()` method is used, which takes an object instance and the method's parameters as arguments. The method is then executed on the specified object.

### Example

To illustrate how to invoke a Java method when given the method name as a string, consider the following example:

```java
public class Example {
    public void helloWorld() {
        System.out.println("Hello World!");
    }
}

public static void main(String[] args) {
    Example example = new Example();
    String methodName = "helloWorld";
    
    // Get the method object
    Method method = example.getClass().getDeclaredMethod(methodName);
    
    // Invoke the method
    method.invoke(example);
}
```

In this example, the `helloWorld()` method is retrieved using the `Class.getDeclaredMethod()` method, and is then invoked using the `Method.invoke()` method.

### Considerations

When using the Reflection API to invoke a Java method when given the method name as a string, there are several considerations to keep in mind.

First, the method must be public in order for it to be accessible via reflection. If the method is not public, an `IllegalAccessException` will be thrown.

Second, the method must be declared in the same class as the object instance on which it is to be invoked. If the method is declared in a superclass, an `NoSuchMethodException` will be thrown.

Finally, the method must have the correct parameters in order for it to be invoked successfully. If the parameters are incorrect, an `IllegalArgumentException` will be thrown.
