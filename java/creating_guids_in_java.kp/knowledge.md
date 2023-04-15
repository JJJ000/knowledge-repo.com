---
title: Generate a uuid in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, a GUID can be created using the java.util.UUID class, which provides a static factory method to generate a type 4 (random) UUID.
---

**Contents**

[TOC]

`**` Generate a GUID**

The following code can be used to generate a GUID in Java:

```java
UUID uuid = UUID.randomUUID();
String randomUUIDString = uuid.toString();
```

`**` Output**

The output of the code above is a randomly generated UUID string. For example:

`3e3b2a2f-d9d3-4e2d-b1e1-47f7e2d2a08f`

`**` Format**

A UUID is a 128-bit number represented as a string of 32 hexadecimal digits in five groups separated by hyphens. It has the following format:

`xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`

`**` Usage**

UUIDs are often used as identifiers in software development and can be used to uniquely identify a record in a database, an object in a system, or any other entity.
