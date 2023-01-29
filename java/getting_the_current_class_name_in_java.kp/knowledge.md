---
title: What is the name of the current Java class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The current class name can be retrieved using the getClass() method.
---

**Contents**

[TOC]

### Using Class.forName()

```java
String className = Class.forName(Thread.currentThread().getStackTrace()[1].getClassName()).getSimpleName();
```

### Using getClass()

```java
String className = this.getClass().getSimpleName();
```

### Using getClassName()

```java
String className = Thread.currentThread().getStackTrace()[1].getClassName();
```
