---
title: What is the process for assigning environment variables from java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can set environment variables from Java using the System.setProperty() method.
---

**Contents**

[TOC]

### Setting Environment Variables

1. Use the `System.getenv()` method to get the environment variables from the system.
2. Use the `System.setenv()` method to set the environment variables in the system.

### Example

```java
String path = System.getenv("PATH");
System.setenv("PATH", path + ":/my/new/path");
```

### Caveats

1. The `System.setenv()` method works only on Windows and Linux systems.
2. The environment variables set using `System.setenv()` will only be available to the current Java process and its child processes.
