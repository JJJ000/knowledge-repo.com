---
title: What is the process of verifying an exception is thrown in junit 5?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Assertions.assertThrows() can be used to assert that an exception is thrown.
---

**Contents**

[TOC]

`**` Overview**

JUnit 5 provides a number of features to help developers test the expected behavior of their code, including the ability to assert that an exception is thrown. This is useful for testing that the code is behaving as expected when an exception occurs.

`**` Asserting an Exception is Thrown**

The JUnit 5 API provides the `assertThrows()` method for asserting that an exception is thrown. This method takes two parameters: the type of exception to be thrown and a `Executable` that contains the code to be tested. The `Executable` can be a lambda expression, a method reference, or an anonymous inner class.

For example, the following code checks that an `IllegalArgumentException` is thrown when the `divide()` method is called with a zero value:

```java
@Test
public void testDivideByZeroThrowsException() {
    assertThrows(IllegalArgumentException.class, () -> divide(10, 0));
}
```

`**` Asserting the Exception Message**

The `assertThrows()` method also allows developers to assert that the exception thrown has the expected message. This is done by passing a `Supplier` as an additional parameter. The `Supplier` should return a `String` containing the expected exception message.

For example, the following code checks that an `IllegalArgumentException` is thrown with the expected message when the `divide()` method is called with a zero value:

```java
@Test
public void testDivideByZeroThrowsException() {
    assertThrows(IllegalArgumentException.class, () -> divide(10, 0),
        () -> "Division by zero should throw an exception");
}
```

`**` Conclusion**

JUnit 5 provides a number of features to help developers test their code, including the ability to assert that an exception is thrown. The `assertThrows()` method allows developers to check that the expected exception is thrown, as well as to assert the expected exception message. This can help ensure that the code is behaving as expected when an exception occurs.
