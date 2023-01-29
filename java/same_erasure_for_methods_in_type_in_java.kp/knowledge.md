---
title: The erasure of the method is the same as that of another method in the same type
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, two methods in the same type can have the same erasure.
---

**Contents**

[TOC]

### Yes

When two methods have the same erasure, it means that they have the same type signature. In Java, this occurs when two methods have the same name and the same parameter types, regardless of the return type.

### Example

For example, consider the following two methods:

```java
public int foo(int a, int b) {
    return a + b;
}

public String foo(int a, int b) {
    return String.valueOf(a + b);
}
```

These two methods have the same erasure, because they have the same name and the same parameter types (both `int`). The return types are different, but that does not affect the erasure.

### Why

The reason for this behavior is that in Java, the type of a method is determined by the combination of its name and parameter types, and not by the return type. This means that when two methods have the same name and parameter types, they are considered to have the same type, regardless of the return type.
