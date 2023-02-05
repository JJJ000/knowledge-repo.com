---
title: What is the Java equivalent of the typedef keyword in c++?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, there is no equivalent keyword to typedef in Java; however, classes can be used to achieve similar behavior.
---

**Contents**

[TOC]

### Java Type Aliases

Java does not have an equivalent keyword to C++'s typedef, but type aliases can be created using the `import static` statement. This statement allows a fully qualified type name to be assigned an alias.

For example, the following statement will create an alias for the `java.util.ArrayList` type:

```java
import static java.util.ArrayList as List;
```

The alias can then be used instead of the fully qualified type name:

```java
List<String> list = new List<>();
```

### Using Interfaces

Another way to achieve a similar effect is to use interfaces. This technique is commonly used to create type aliases for generic types.

For example, the following interface creates an alias for a `Map` with `String` keys and `Integer` values:

```java
public interface StringIntegerMap extends Map<String, Integer> {}
```

The interface can then be used as a type alias:

```java
StringIntegerMap map = new HashMap<>();
```

### Using Classes

Similar to interfaces, classes can be used to create type aliases. The main difference is that classes can contain implementation code, while interfaces cannot.

For example, the following class creates an alias for a `Map` with `String` keys and `Integer` values:

```java
public class StringIntegerMap extends HashMap<String, Integer> {}
```

The class can then be used as a type alias:

```java
StringIntegerMap map = new StringIntegerMap();
```
