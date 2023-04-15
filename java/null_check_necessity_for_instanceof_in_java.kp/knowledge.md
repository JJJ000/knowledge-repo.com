---
title: Do you need to check if something is null before using the 'instanceof' operator?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, null check is not needed before calling instanceof in Java.
---

**Contents**

[TOC]

### No

Instanceof does not throw any NullPointerException when used with a null argument. According to the Java Language Specification, the result of instanceof is false when the object reference being compared is null.

### Usage

The instanceof operator is used to test if the object or instance is an instanceof the specified type. It is used to check if an object belongs to a particular class or a subclass or an interface.

### Example

```java
String str = null;
System.out.println(str instanceof String); // Output false
```

### Conclusion

In conclusion, a null check is not needed before calling instanceof in Java.
