---
title: What is the equivalent of .net's notimplementedexception in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, a NotImplementedException can be thrown by using the UnsupportedOperationException class.
---

**Contents**

[TOC]

### java.lang.UnsupportedOperationException

The `UnsupportedOperationException` is the closest analog to .NET's `NotImplementedException` in Java. This exception is thrown when a method is invoked that is not implemented yet, or is not supported by the current implementation.

### java.lang.UnsupportedOperationException Usage

The `UnsupportedOperationException` is typically used in abstract classes or interfaces where a method is declared but not implemented. It is also used when a method is not supported in the current implementation. When this exception is thrown, it indicates that the method is not supported and should not be used.

### java.lang.UnsupportedOperationException Example

The following code snippet shows an example of how to use the `UnsupportedOperationException` in Java:

```java
public class MyClass {
    public void doSomething() {
        throw new UnsupportedOperationException("This method is not supported in the current implementation");
    }
}
```

### Conclusion

The `UnsupportedOperationException` is the closest analog to .NET's `NotImplementedException` in Java. This exception is typically used in abstract classes or interfaces where a method is declared but not implemented, or when a method is not supported in the current implementation. When this exception is thrown, it indicates that the method is not supported and should not be used.
