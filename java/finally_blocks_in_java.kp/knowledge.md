---
title: Will a finally block always be executed in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Yes, a finally block in Java will always be executed regardless of any exceptions.
---

**Contents**

[TOC]

### Yes

A finally block is always executed in Java, regardless of whether an exception is thrown or not. This makes it an ideal place to perform any necessary clean-up tasks, such as closing a file or releasing a database connection.

### Why It's Important

The finally block is important because it ensures that any necessary clean-up tasks are always performed, even if an exception is thrown. This helps to prevent resource leaks, which can cause memory leaks and other problems.

### Usage

The finally block is typically used in conjunction with a try/catch block. The try block is used to execute code that may throw an exception, and the catch block is used to handle the exception if one is thrown. The finally block is then used to perform any necessary clean-up tasks, such as closing a file or releasing a database connection.

### Example

For example, consider the following code:

```java
try {
    // code that may throw an exception
} catch (Exception e) {
    // handle the exception
} finally {
    // perform any necessary clean-up tasks
}
```

In this example, the code in the try block may throw an exception, which will be handled by the catch block. Regardless of whether an exception is thrown or not, the finally block will always be executed to perform any necessary clean-up tasks.
