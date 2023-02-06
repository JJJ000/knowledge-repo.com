---
title: Removal of the permanent generation memory space in Java development kit 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: JDK 8 introduced the metaspace, which replaces the PermGen space, eliminating the need for manual PermGen tuning.
---

**Contents**

[TOC]

#### Introduction
PermGen (Permanent Generation) is a feature of the Java Virtual Machine (JVM) which stores class definitions and associated metadata. It was introduced in Java 5 and was removed in Java 8.

#### Reasons for Removal
PermGen was removed in Java 8 due to its high memory usage, which caused performance issues and OutOfMemoryErrors. Additionally, PermGen was difficult to configure and maintain, as it had to be tuned to fit the application's needs.

#### Alternatives
In Java 8, PermGen was replaced by the Metaspace, which stores class definitions and associated metadata in native memory. This allows for better memory usage and is easier to configure and maintain.

#### Conclusion
PermGen was removed in Java 8 due to its high memory usage, difficulty to configure and maintain, and performance issues. It was replaced by the Metaspace, which stores class definitions and associated metadata in native memory and is easier to configure and maintain.
