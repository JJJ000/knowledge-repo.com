---
title: Which Java exception should be thrown for an unsupported or unimplemented operation?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The UnsupportedOperationException is the standard exception to throw in Java for not supported/implemented operations.
---

**Contents**

[TOC]

### UnsupportedOperationException
The UnsupportedOperationException is the standard exception to throw in Java for not supported/implemented operations. It is a RuntimeException which indicates that a requested operation is not supported.

### When to Throw
This exception should be thrown when an operation is requested that is not supported or implemented. This can happen when a method is invoked on a class that does not support the operation, or when an operation is attempted that is not implemented.

### Example
For example, consider a class that implements the `List` interface but does not support the `add` operation. If a user attempts to call the `add` method on this class, an UnsupportedOperationException should be thrown.

### Handling
When handling this exception, the program should provide an appropriate error message to the user. Additionally, the program should be designed to avoid invoking unsupported operations.
