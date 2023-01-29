---
title: What should I use instead of handler() now that it is no longer supported?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The recommended replacement for Handler() in Java is the HandlerThread class.
---

**Contents**

[TOC]

### Answer

### Java SE 7

In Java SE 7, the `java.util.logging.Handler` class is still available. However, it is recommended to use the `java.util.logging.Logger` class instead. This class provides improved logging capabilities and is more flexible than the `Handler` class.

### Java SE 8

In Java SE 8, the `java.util.logging.Handler` class has been deprecated and replaced with the `java.util.logging.Logger` class. The `Logger` class provides improved logging capabilities and is more flexible than the `Handler` class.

### Alternatives

In addition to the `Logger` class, there are a number of other logging frameworks available. These include Log4j, SLF4J, and Logback. Each of these frameworks provides a different set of features and capabilities. It is recommended to research each of these frameworks to determine which one best fits your needs.

### Conclusion

The `java.util.logging.Handler` class has been deprecated in Java SE 8 and replaced with the `java.util.logging.Logger` class. There are also a number of other logging frameworks available that may provide better features and capabilities than the `Logger` class. It is recommended to research each of these frameworks to determine which one best fits your needs.
