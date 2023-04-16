---
title: Stop execution when an exception is encountered
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The program will stop executing and the exception will be thrown.
---

**Contents**

[TOC]

### Using try-catch-finally

The most common way to break when an exception is thrown in Java is to use a `try-catch-finally` block. In the `try` block, code is executed that could potentially throw an exception. If an exception is thrown, the `catch` block is executed and the code in the `finally` block is executed regardless. The `finally` block is typically used to clean up any resources that were used in the `try` block.

### Using throws

Another way to break when an exception is thrown in Java is to use the `throws` keyword. The `throws` keyword is used to declare that a method can throw an exception. Any code that calls a method declared with `throws` must either handle the exception or declare that it throws the same exception.

### Using System.exit()

The `System.exit()` method can also be used to break when an exception is thrown in Java. This method exits the application immediately, and any code after the call to `System.exit()` will not be executed. This should be used with caution, as it can lead to unexpected behavior.

### Using break

The `break` keyword can also be used to break when an exception is thrown in Java. This keyword is typically used to break out of a loop, but it can also be used to break out of a `try-catch` block. This should be used with caution, as it can lead to unexpected behavior.
