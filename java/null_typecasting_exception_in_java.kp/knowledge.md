---
title: There are no issues when performing type casting with a null value in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No exception is thrown when typecasting a null in Java.
---

**Contents**

[TOC]

## NullPointerException

When a typecast is attempted with a null value, a `NullPointerException` is thrown. This is because the `null` value does not refer to an object, so the typecast is not valid.

## Example

The following code snippet throws a `NullPointerException` when the typecast is attempted:

```java
Object obj = null;
String str = (String) obj;
```

## Handling the Exception

The `NullPointerException` should be handled by using the `instanceof` operator to check if the object is null before attempting the typecast. For example:

```java
Object obj = null;
if (obj instanceof String) {
  String str = (String) obj;
}
```

## Alternatives

Another option is to use the `Objects.requireNonNull()` method to check if the object is null before attempting the typecast. For example:

```java
Object obj = null;
String str = (String) Objects.requireNonNull(obj);
```
