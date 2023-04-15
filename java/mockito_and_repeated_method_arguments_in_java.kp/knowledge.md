---
title: Is it possible for mockito to record the arguments of a method that has been called multiple times?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, Mockito can capture arguments of a method called multiple times using ArgumentCaptor.
---

**Contents**

[TOC]

### Yes
Mockito is able to capture arguments of a method called multiple times in Java. This is done by using the `ArgumentCaptor` class.

### How It Works
The `ArgumentCaptor` class is used to capture arguments for mocked methods. It works by creating an instance of the `ArgumentCaptor` class and passing it to the `when` method of the Mockito API. This will then capture the arguments of any method calls that are made with the same instance of the `ArgumentCaptor` class.

### Example
For example, consider the following code:
```java
MyClass myClass = mock(MyClass.class);
ArgumentCaptor<String> argCaptor = ArgumentCaptor.forClass(String.class);
when(myClass.someMethod(argCaptor.capture())).thenReturn(true);

myClass.someMethod("foo");
myClass.someMethod("bar");

List<String> capturedArgs = argCaptor.getAllValues();
// capturedArgs = ["foo", "bar"]
```
In this example, the `ArgumentCaptor` instance is used to capture the arguments of the `someMethod` method that is called twice, once with the argument `"foo"` and once with the argument `"bar"`. The captured arguments are then stored in a `List` and can be accessed via the `getAllValues` method.

### Conclusion
Mockito is able to capture arguments of a method called multiple times in Java by using the `ArgumentCaptor` class. This is a useful tool for verifying the arguments of a method are being called correctly.
