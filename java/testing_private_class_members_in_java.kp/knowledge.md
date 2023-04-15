---
title: What is the best way to evaluate the performance of a class that has private methods, fields, or inner classes?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use reflection to access and test private methods, fields, and inner classes in Java.
---

**Contents**

[TOC]

### Unit Testing
Unit testing is the most common way to test a class with private methods, fields or inner classes in Java. This involves using a unit testing framework like JUnit or Mockito to create test cases that check the behavior of the class under test. The tests should cover all the public methods of the class and any private methods that are used by the public methods.

### Access Modifiers
The access modifiers of the private methods and fields can be changed to package-private or protected to allow the test classes to access them. This should only be done if the private methods or fields are not part of the class’s implementation details and are required for testing.

### Reflection
Reflection can be used to access private methods and fields in Java. This should only be used if the access modifiers cannot be changed and if the private methods or fields are necessary for testing.

### Test Doubles
Test doubles like mocks, stubs, and spies can be used to test private methods and fields in Java. This should only be done if the private methods or fields are not part of the class’s implementation details and are required for testing.
