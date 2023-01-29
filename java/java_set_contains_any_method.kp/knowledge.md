---
title: Is there an equivalent of 'contains any' for Java sets?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Java Set interface provides the containsAll() method to check if a Set contains any elements of another Set.
---

**Contents**

[TOC]

### containsAny()
The `containsAny()` method can be used to determine if a Java Set contains any of the elements in a given collection.

### Syntax
The syntax for the `containsAny()` method is:
```java
boolean containsAny(Collection<?> c)
```

### Parameters
The `containsAny()` method takes a single parameter:
- c: The collection to be tested for containment in the set

### Return Value
The `containsAny()` method returns a boolean value indicating whether any of the elements in the given collection are present in the set.
