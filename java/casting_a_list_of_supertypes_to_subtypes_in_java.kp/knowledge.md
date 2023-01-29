---
title: What is the process of converting a list of supertypes to a list of subtypes?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can cast a List of supertypes to a List of subtypes by using the `List<? extends Subtype>` syntax.
---

**Contents**

[TOC]

### Using Generics

Generics can be used to cast a list of supertypes to a list of subtypes. The syntax for this is as follows:

```java
List<Subtype> subtypeList = (List<Subtype>) supertypeList;
```

This will cast the `supertypeList` to a `List<Subtype>` and assign it to the `subtypeList` variable.

### Using Stream Mapping

Stream mapping can also be used to cast a list of supertypes to a list of subtypes. The syntax for this is as follows:

```java
List<Subtype> subtypeList = supertypeList.stream()
                                        .map(item -> (Subtype) item)
                                        .collect(Collectors.toList());
```

This will create a stream from the `supertypeList` and map each item to a `Subtype`, then collect the result into a `List<Subtype>` and assign it to the `subtypeList` variable.

### Using For-Loop

A for-loop can be used to cast a list of supertypes to a list of subtypes. The syntax for this is as follows:

```java
List<Subtype> subtypeList = new ArrayList<>();
for (Supertype item : supertypeList) {
    subtypeList.add((Subtype) item);
}
```

This will iterate over the `supertypeList` and cast each item to a `Subtype` and add it to the `subtypeList` list.
