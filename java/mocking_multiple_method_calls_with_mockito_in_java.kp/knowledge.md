---
title: Making multiple invocations of the same method with the same parameters using mockito
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Mockito can be used to stub the same method with the same arguments multiple times using the `doAnswer()` or `doReturn()` methods.
---

**Contents**

[TOC]

### Setting Up the Mock

The first step is to set up the Mockito mock object. This can be done using the `Mockito.mock` method:

```java
MyClass mockObject = Mockito.mock(MyClass.class);
```

### Setting Up the Stub

Once the mock object has been created, it can then be used to stub a particular method call. This can be done using the `Mockito.when` method:

```java
Mockito.when(mockObject.someMethod(arg1, arg2)).thenReturn(someValue);
```

### Making the Calls

Once the stub has been set up, the mock object can then be used to make multiple calls to the same method with the same arguments. This can be done using the `Mockito.verify` method:

```java
mockObject.someMethod(arg1, arg2);
mockObject.someMethod(arg1, arg2);
```

### Verifying the Calls

Finally, the calls that were made to the mock object can be verified using the `Mockito.verify` method:

```java
Mockito.verify(mockObject, Mockito.times(2)).someMethod(arg1, arg2);
```

This will verify that the method was called twice with the same arguments.
