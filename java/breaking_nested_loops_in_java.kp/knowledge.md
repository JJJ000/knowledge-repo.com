---
title: What is the best way to exit multiple levels of loops in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use the keyword `break` to exit out of the innermost loop.
---

**Contents**

[TOC]

### Using Labels

Java provides a way to break out of nested loops using labels. A label is a name given to a block of code. Labels are used in conjunction with the `break` statement to allow a program to break out of a labeled block of code.

To use labels, the first step is to label the block of code you want to break out of. This is done by placing the label before the loop. For example, the following code labels a `while` loop with the label `outer`:

```java
outer:
while (condition) {
    // code
}
```

The next step is to use the `break` statement with the label. The `break` statement can be used to break out of any labeled block of code. For example, the following code will break out of the `outer` loop:

```java
if (condition) {
    break outer;
}
```

### Using Return

Another way to break out of nested loops in Java is to use the `return` statement. The `return` statement can be used to immediately exit a method, which will also break out of any loops in the method.

For example, the following code will break out of the nested loops and return from the method:

```java
if (condition) {
    return;
}
```

### Using Exceptions

Java also provides a way to break out of nested loops using exceptions. Exceptions are special objects that are thrown when an error occurs. Exceptions can be caught and handled, or they can be thrown again to break out of a loop.

To use exceptions to break out of a loop, the first step is to create an exception object. This is done with the `new` keyword. For example, the following code creates an `IllegalArgumentException` object:

```java
IllegalArgumentException e = new IllegalArgumentException();
```

The next step is to throw the exception. This is done with the `throw` keyword. For example, the following code will throw the `IllegalArgumentException` object:

```java
if (condition) {
    throw e;
}
```

The exception will then be thrown and caught by the loop, which will break out of the loop.
