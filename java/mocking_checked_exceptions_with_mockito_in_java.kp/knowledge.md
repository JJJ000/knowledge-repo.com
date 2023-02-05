---
title: Have mockito throw checked exceptions
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Mockito cannot throw checked Exceptions, but you can use the doThrow() method to simulate throwing an Exception.
---

**Contents**

[TOC]

# Section 1: Setup

Using Mockito, you can throw checked Exceptions from mocks by using the `when` and `thenThrow` methods.

# Section 2: Syntax

The syntax for throwing a checked Exception from a mock is as follows:

```
when(mockObject.methodName(any(parameterType.class))).thenThrow(new ExceptionType(message));
```

# Section 3: Example

For example, to throw an `IllegalArgumentException` from a mock object:

```
when(mockObject.methodName(any(String.class))).thenThrow(new IllegalArgumentException("message"));
```

# Section 4: Considerations

It is important to note that when throwing checked Exceptions from mocks, the code calling the mocked method must be prepared to handle the Exception. If the Exception is not handled, the code will fail to compile.
