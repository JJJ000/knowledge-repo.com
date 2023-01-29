---
title: What is the best way to use mockito to simulate void methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can mock void methods with the answer() or doAnswer() methods.
---

**Contents**

[TOC]

### Using doAnswer()
Mockito provides the ability to mock void methods with the help of doAnswer() method. This method allows stubbing with generic Answer interface. The Answer interface requires us to implement the answer() method, which then allows us to stub a void method with generic behavior.

### Example

The following example demonstrates how to mock a void method in Mockito:

```java
// mocking void methods
doAnswer(invocation -> {
    Object argument = invocation.getArgument(0);
    // perform some operation
    return null;
}).when(mock).someVoidMethod(any());
```

### Using doThrow()
Mockito also provides the ability to mock void methods with the help of doThrow() method. This method allows us to stub the void methods with an exception.

### Example

The following example demonstrates how to mock a void method in Mockito using doThrow():

```java
// mocking void methods
doThrow(new RuntimeException()).when(mock).someVoidMethod();
```
