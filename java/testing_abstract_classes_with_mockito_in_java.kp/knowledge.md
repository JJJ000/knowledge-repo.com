---
title: Testing abstract classes using mockito
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Mockito can be used to create mock objects of abstract classes and test their methods.
---

**Contents**

[TOC]

### Overview
Mockito is a Java-based mocking framework used for unit testing. It is typically used to create mock objects for testing purposes. Mockito can be used to test abstract classes in Java by creating a mock object of the abstract class. The mock object can then be used to test the behavior of the abstract class and its methods.

### Creating a Mock Object
To create a mock object of an abstract class, the Mockito framework must be used. The Mockito.mock() method can be used to create a mock object of the abstract class. The method takes the class type as its argument and returns a mock object of the class.

### Testing the Abstract Class
Once the mock object is created, it can be used to test the behavior of the abstract class and its methods. This can be done by setting up the mock object with the expected behavior, then verifying that the behavior is correct. Mockito provides several methods for setting up the mock object, such as when(), thenReturn(), and verify().

### Conclusion
Mockito can be used to test abstract classes in Java by creating a mock object of the abstract class and setting up the expected behavior. The mock object can then be used to verify that the behavior of the abstract class and its methods is correct.
