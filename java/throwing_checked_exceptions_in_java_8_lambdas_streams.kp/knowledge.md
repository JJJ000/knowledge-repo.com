---
title: What is the most effective way to throw checked exceptions from within Java 8 lambdas/streams?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `throw` keyword to throw a checked exception from inside a lambda/stream.
---

**Contents**

[TOC]

### Option 1: Using a Wrapper

One way to throw a checked exception from inside a lambda or stream is to wrap the code that is throwing the exception within a try-catch block. The code within the try-block is the code that may throw the checked exception. The catch block can then be used to handle the exception, such as by re-throwing it.

For example, the following code snippet shows how a checked exception can be thrown from inside a lambda expression:

```
myList.stream()
      .map(element -> {
          try {
              // Code that may throw a checked exception
              return doSomething(element);
          } catch (MyCheckedException e) {
              throw e;
          }
      })
      .collect(Collectors.toList());
```

### Option 2: Using an Exception-Throwing Function

Another way to throw a checked exception from inside a lambda or stream is to use an exception-throwing function. This is a function that takes a parameter and may throw a checked exception. The lambda or stream can then call this function and handle the exception as needed.

For example, the following code snippet shows how a checked exception can be thrown from inside a stream:

```
myList.stream()
      .map(element -> doSomethingThatThrowsException(element))
      .collect(Collectors.toList());
```

### Option 3: Using a Checked Exception Wrapper

A third option to throw a checked exception from inside a lambda or stream is to use a checked exception wrapper. This is a wrapper class that wraps a checked exception and allows it to be thrown from within a lambda or stream.

For example, the following code snippet shows how a checked exception can be thrown from inside a stream using a checked exception wrapper:

```
myList.stream()
      .map(element -> {
          try {
              // Code that may throw a checked exception
              return doSomething(element);
          } catch (MyCheckedException e) {
              throw new CheckedExceptionWrapper(e);
          }
      })
      .collect(Collectors.toList());
```

### Option 4: Using a Custom Collector

A fourth option to throw a checked exception from inside a lambda or stream is to use a custom collector. This is a collector that can be used to collect the results of a stream and also handle any checked exceptions that may be thrown.

For example, the following code snippet shows how a checked exception can be thrown from inside a stream using a custom collector:

```
myList.stream()
      .collect(MyCustomCollector.of(
          // Code that may throw a checked exception
          () -> doSomething(), 
          (a, b) -> doSomethingElse(a, b)));
```
