---
title: What is the reason that mockito does not provide mocking of static methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Mockito cannot mock static methods because static methods are part of a class, not an instance of a class.
---

**Contents**

[TOC]

1. **Static Methods are Not Virtual**
Static methods are not virtual, meaning they are not overridden when a class is extended. Therefore, when a static method is called from a mock object, the actual method will be executed, rather than the mocked one.

2. **Static Methods Cannot be Intercepted**
Mockito uses a technique called "bytecode manipulation" to intercept method calls and replace them with mocked behavior. Since static methods cannot be overridden, they cannot be intercepted by Mockito.

3. **Alternatives to Mocking Static Methods**
There are alternative methods to mocking static methods. One option is to use PowerMock, which is an extension of Mockito that provides support for mocking static methods. Another option is to refactor the code to make the static method an instance method and then mock it as usual.

4. **Conclusion**
Mockito does not support mocking static methods because static methods are not virtual and cannot be intercepted. However, there are alternative methods to mocking static methods, such as using PowerMock or refactoring the code.
