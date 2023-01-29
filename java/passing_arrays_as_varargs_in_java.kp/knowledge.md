---
title: Is it possible to pass an array as an argument to a method with variable arguments in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, you can pass an array as arguments to a method with variable arguments in Java.
---

**Contents**

[TOC]

**Yes**

**Method Definition**
Methods with variable arguments are declared with an ellipsis (...) as the last parameter in the method signature. For example:

```java
public void myMethod(String... args) {
    // Method body
}
```

**Passing an Array**
An array can be passed as an argument to a method with variable arguments by simply passing the array as the argument. For example:

```java
String[] myArray = {"a", "b", "c"};
myMethod(myArray);
```

**Internally**
Internally, the passed array is converted to a sequence of individual arguments. For example, the above code would be equivalent to:

```java
myMethod("a", "b", "c");
```

**Benefits**
Passing an array as an argument to a method with variable arguments can be beneficial when the size of the array is unknown or when there is a need to pass a variable number of arguments to a method.
