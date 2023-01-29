---
title: What is the process for logging a message with formatting, an array of objects, and an exception?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Logger.log() method to log formatted messages, object arrays, and exceptions in Java.
---

**Contents**

[TOC]

### Logging Formatted Messages

Logging formatted messages in Java is done using the `String.format()` method. This method allows you to create a string with placeholders for variables, and then pass in the variables as arguments. For example, to log a message with two variables, you could write:

```java
String message = String.format("The value of x is %d and the value of y is %d", x, y);
logger.info(message);
```

### Logging Object Arrays

Logging object arrays in Java is done using the `Arrays.toString()` method. This method takes an array of objects as an argument and returns a string representation of the array. For example, to log an array of integers, you could write:

```java
int[] array = {1, 2, 3};
logger.info(Arrays.toString(array));
```

### Logging Exceptions

Logging exceptions in Java is done using the `Logger.log()` method. This method takes an exception object as an argument and logs it to the logger. For example, to log an exception, you could write:

```java
try {
    // some code
} catch (Exception e) {
    logger.log(e);
}
```

### Logging Exception Stack Traces

Logging an exception stack trace in Java is done using the `Logger.log()` method. This method takes an exception object as an argument and logs its stack trace to the logger. For example, to log an exception stack trace, you could write:

```java
try {
    // some code
} catch (Exception e) {
    logger.log(e.getStackTrace());
}
```
