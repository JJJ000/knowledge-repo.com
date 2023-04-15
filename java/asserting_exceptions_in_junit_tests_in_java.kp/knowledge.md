---
title: What evidence do you have to demonstrate that a particular exception is thrown in JUnit tests?
authors:
- nanja_dev
tags:
- java
- junit
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JUnit tests, an exception can be asserted by using the assertThrows() method.
---

**Contents**

[TOC]

### Asserting Exception with try/catch

The most common way to assert that a certain exception is thrown in JUnit tests is to use a try/catch block. This involves wrapping the code that is expected to throw an exception in a try block and then catching the exception in a catch block. The catch block can then be used to check that the expected exception was thrown.

```java
try {
   // code expected to throw an exception
} catch (SomeException e) {
   // assert that the expected exception was thrown
}
```

### Asserting Exception with @Test Annotation

Another way to assert that a certain exception is thrown in JUnit tests is to use the @Test annotation. This annotation can be used to specify the expected exceptions that should be thrown when running a test. The expected exceptions can be specified by using the 'expected' attribute of the @Test annotation.

```java
@Test(expected=SomeException.class)
public void testSomeException() {
   // code expected to throw an exception
}
```

### Asserting Exception with assertThrows()

The assertThrows() method can also be used to assert that a certain exception is thrown in JUnit tests. This method takes two arguments: the expected exception class and a lambda expression that contains the code that is expected to throw the exception. If the code does not throw the expected exception, the test will fail.

```java
assertThrows(SomeException.class, () -> {
   // code expected to throw an exception
});
```
