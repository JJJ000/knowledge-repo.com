---
title: What is the best way to reset a stringbuilder?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The StringBuilder can be cleared by calling its .delete(0, length) method.
---

**Contents**

[TOC]

### Method 1: Replace the Contents

The simplest way to clear a `StringBuilder` is to replace its contents with an empty string. This can be done using the `replace` method:

```java
StringBuilder sb = new StringBuilder("This is a test");
sb.replace(0, sb.length(), "");
```

### Method 2: Set Length to Zero

The `StringBuilder` class also provides a `setLength` method which can be used to set the length of the `StringBuilder` to zero:

```java
StringBuilder sb = new StringBuilder("This is a test");
sb.setLength(0);
```

### Method 3: Create a New Instance

A third way to clear a `StringBuilder` is to simply create a new instance:

```java
StringBuilder sb = new StringBuilder("This is a test");
sb = new StringBuilder();
```
