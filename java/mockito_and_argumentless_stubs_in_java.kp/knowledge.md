---
title: Is it possible for mockito to stub a method without taking the argument into consideration?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, Mockito can stub a method without regard to the argument using the any() matcher.
---

**Contents**

[TOC]

Yes, Mockito can stub a method without regard to the argument in Java.

### Stubbing a Method

Mockito can stub a method without regard to the argument by using the `any()` matcher. This matcher matches any argument passed to the method, regardless of type. The following example shows how to stub a method without regard to the argument:

```java
when(mockObject.someMethod(any())).thenReturn("some value");
```

### Verifying a Method

Mockito can also verify a method without regard to the argument by using the `any()` matcher. The following example shows how to verify a method without regard to the argument:

```java
verify(mockObject).someMethod(any());
```

### Additional Resources

For more information on stubbing and verifying methods with Mockito, see the [Mockito documentation](http://site.mockito.org/).
