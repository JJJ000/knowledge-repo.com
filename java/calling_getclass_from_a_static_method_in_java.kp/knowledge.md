---
title: What is the syntax for calling the getclass() method from a static method in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: From a static method, getClass() can be called using the keyword `this`.
---

**Contents**

[TOC]

### What is getClass()?
The getClass() method is a method in Java that returns the runtime class of an object. It is defined in the Object class and is accessible to all Java objects.

### How to call getClass() from a static method
When calling getClass() from a static method, you must first obtain an instance of the class in order to call the getClass() method. This can be done using the Class.forName() method, which takes a string parameter containing the name of the class to be instantiated.

### Example
For example, if you have a static method in the class MyClass and you want to call getClass() from it, you can do so as follows:

```java
public static void myStaticMethod() {
    Class<?> clazz = Class.forName("MyClass");
    Class<?> myClass = clazz.getClass();
    // Do something with the myClass instance
}
```

### Conclusion
In summary, to call getClass() from a static method in Java, you must first obtain an instance of the class using the Class.forName() method. Once you have an instance of the class, you can then call the getClass() method.
