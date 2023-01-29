---
title: Throwing exceptions in Java while preserving the stack trace
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Exceptions can be rethrown in Java using the `throw` keyword, preserving the original stack trace.
---

**Contents**

[TOC]

### Using try/catch/finally

The most common way of rethrowing an exception in Java is by using the try/catch/finally structure. In this structure, the try block is used to catch the exception, while the catch block is used to handle the exception. The finally block is then used to rethrow the exception, while preserving the stack trace.

```java
try {
    // code that may throw an exception
} catch (Exception e) {
    // handle the exception
} finally {
    throw e;
}
```

### Using Throwables

Another way of rethrowing an exception in Java is by using the Throwables class. The Throwables class provides a method called rethrow that can be used to rethrow an exception, while preserving the stack trace.

```java
try {
    // code that may throw an exception
} catch (Exception e) {
    // handle the exception
    Throwables.rethrow(e);
}
```

### Using Exceptions

A third way of rethrowing an exception in Java is by using the Exceptions class. The Exceptions class provides a method called rethrow that can be used to rethrow an exception, while preserving the stack trace.

```java
try {
    // code that may throw an exception
} catch (Exception e) {
    // handle the exception
    Exceptions.rethrow(e);
}
```

### Using Throwable's initCause

A final way of rethrowing an exception in Java is by using the Throwable's initCause method. This method can be used to rethrow an exception, while preserving the stack trace.

```java
try {
    // code that may throw an exception
} catch (Exception e) {
    // handle the exception
    Throwable t = new Throwable();
    t.initCause(e);
    throw t;
}
```
