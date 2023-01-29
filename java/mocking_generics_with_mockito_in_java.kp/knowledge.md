---
title: Mocking classes with generic parameters using mockito
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can mock classes with generic parameters by using the Mockito.spy() method.
---

**Contents**

[TOC]

### Section 1 - What is Mockito? 
Mockito is a popular open source mocking framework for Java. It is used to create mock objects for testing purposes. Mockito allows developers to mock out interfaces and classes, including those with generic parameters.

### Section 2 - How to Mock Classes with Generic Parameters
Mocking classes with generic parameters in Mockito is done by using the `Mockito.mock()` method. This method takes a Class object as a parameter and returns a mocked instance of the class. The generic type of the class can be specified using the `Mockito.withSettings()` method. This method takes a MockSettings object as a parameter and returns a new MockSettings object with the generic type specified.

### Section 3 - Example
For example, to mock a class with a generic type of `String`, the following code can be used:

```java
Class<MyClass<String>> clazz = MyClass.class;
MyClass<String> mock = Mockito.mock(clazz, Mockito.withSettings().useConstructor().defaultAnswer(Mockito.RETURNS_DEFAULTS));
```

### Section 4 - Conclusion
Mocking classes with generic parameters in Mockito is a straightforward process. By using the `Mockito.mock()` and `Mockito.withSettings()` methods, developers can easily create mock objects for testing purposes.
