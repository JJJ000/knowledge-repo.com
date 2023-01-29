---
title: Testing a void method with mockito to verify if an exception is thrown
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can be used to verify that the void method throws an expected exception.
---

**Contents**

[TOC]

`**` Setup**

1. Create a mock object of the class whose method is to be tested:

```java
MyClass mockObject = Mockito.mock(MyClass.class);
```

2. Set up the expected exception:

```java
Mockito.doThrow(new Exception()).when(mockObject).myVoidMethod();
```

`**` Execution**

1. Invoke the method to be tested:

```java
mockObject.myVoidMethod();
```

`**` Verification**

1. Verify that the expected exception was thrown:

```java
Mockito.verify(mockObject).myVoidMethod();
```

`**` Cleanup**

1. Reset the mock object:

```java
Mockito.reset(mockObject);
```
