---
title: Verify the arguments of the mockito method
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can be used to verify that the expected arguments were passed to a method invocation.
---

**Contents**

[TOC]

### Using Mockito

Mockito provides a `verify()` method to check that a method was called with certain parameters. The syntax for this is:

```java
Mockito.verify(mockObject).methodName(methodArguments);
```

Where `mockObject` is the mock object, `methodName` is the name of the method that was called, and `methodArguments` is a list of the arguments that were passed to the method.

### Using Hamcrest Matchers

Mockito also provides a way to use Hamcrest matchers to verify that the arguments to a method were correct. The syntax for this is:

```java
Mockito.verify(mockObject).methodName(Mockito.argThat(Matchers.matcher));
```

Where `mockObject` is the mock object, `methodName` is the name of the method that was called, `Matchers.matcher` is the Hamcrest matcher that will be used to verify the arguments, and `Mockito.argThat` is a Mockito argument matcher that will be used to apply the Hamcrest matcher.
