---
title: Using mockito to simulate static methods
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can be used to mock static methods by using the PowerMockito library.
---

**Contents**

[TOC]

### Understanding Static Methods

Static methods are methods that are associated with a class, rather than an instance of a class. They are also known as class methods. These methods can be called directly from the class, without needing to create an instance of the class. Static methods are useful for utility functions or for performing operations that don't require any instance data.

### Benefits of Mocking Static Methods

Mocking static methods can be useful in unit testing, as it allows developers to isolate a unit of code and test it in isolation. This can help to ensure that the code is functioning correctly, without being affected by other parts of the system. Additionally, mocking static methods can help to reduce the complexity of tests, as the developer does not need to set up an instance of the class to test the static method.

### How to Mock Static Methods with Mockito

Mockito is a popular Java mocking framework that can be used to mock static methods. To mock a static method, developers can use the Mockito.mockStatic() method. This method takes the class of the static method as an argument and returns a Mockito mock object. The mock object can then be used to stub the static method, allowing the developer to control the behavior of the method.

### Example of Mocking a Static Method

For example, consider the following class with a static method:

```java
public class UtilityClass {
    public static int getValue() {
        return 5;
    }
}
```

To mock this static method with Mockito, the developer can use the following code:

```java
Mockito.mockStatic(UtilityClass.class);
Mockito.when(UtilityClass.getValue()).thenReturn(10);
```

The first line creates a mock object for the UtilityClass class. The second line stubs the getValue() method, so that it returns 10 instead of 5.
