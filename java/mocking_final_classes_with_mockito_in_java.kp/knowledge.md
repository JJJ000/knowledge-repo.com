---
title: How can I use mockito to create a mock of a final class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito cannot mock final classes, but PowerMock can be used to mock them.
---

**Contents**

[TOC]

### Understanding Final Classes

Final classes are classes that cannot be inherited from, meaning that no other classes can extend it. This is done to ensure that the class remains unchanged. For example, the Java class `String` is a final class, meaning that no other classes can extend it.

### Why Mock Final Classes

Mocking final classes can be useful for testing the behavior of code that uses the class. For example, if a class uses the `String` class to manipulate a string, then mocking the `String` class can help test the behavior of the class.

### Mockito

Mockito is a popular Java mocking framework that can be used to mock final classes. It can be used to create mock objects of the final class, allowing you to test the behavior of code that uses the class.

### Example

Here is an example of using Mockito to mock a final class.

```java
// Create a mock object of the final class
String mockString = Mockito.mock(String.class);

// Set the behavior of the mock object
Mockito.when(mockString.length()).thenReturn(10);

// Test the behavior of the code
int length = mockString.length();
assertEquals(10, length);
```
