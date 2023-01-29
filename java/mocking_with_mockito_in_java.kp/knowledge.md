---
title: Create mock objects using mockito, but do not mock all methods
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can be used to mock certain methods while leaving others intact by selectively applying Mockito`s mock and spy methods.
---

**Contents**

[TOC]

### Setting Up Mockito 
Mockito is a powerful mocking framework for Java. To use Mockito, you must first add it to your project's dependencies. This can be done through a build tool such as Maven or Gradle, or manually by downloading the Mockito jar and adding it to your project's classpath.

### Mocking Methods
Once you have Mockito set up in your project, you can use it to mock methods. To mock a method, you must first create a mock object of the class containing the method you wish to mock. You can then use the `when()` syntax to specify which methods should be mocked. For example:

```java
MyClass mockObject = Mockito.mock(MyClass.class);
when(mockObject.someMethod()).thenReturn("mocked result");
```

This will cause the `someMethod()` method to return the value "mocked result" whenever it is called.

### Not Mocking Methods
If you do not want to mock a particular method, you can simply not specify it in the `when()` syntax. For example:

```java
MyClass mockObject = Mockito.mock(MyClass.class);
when(mockObject.someMethod()).thenReturn("mocked result");
```

In this example, the `someMethod()` method will be mocked, but any other methods in the `MyClass` class will not be mocked.

### Verifying Mocks
Once you have mocked the methods you want, you can use Mockito's `verify()` method to ensure that the mocked methods are being called as expected. For example:

```java
MyClass mockObject = Mockito.mock(MyClass.class);
when(mockObject.someMethod()).thenReturn("mocked result");

// Call the method
String result = mockObject.someMethod();

// Verify that the method was called
verify(mockObject).someMethod();
```

This will verify that the `someMethod()` method was called at least once.
