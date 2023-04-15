---
title: What are the key distinctions between running Java with the '-server' flag and the '-client' flag?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: `java -server` optimizes for long-running applications, while `java -client` optimizes for applications with a faster startup time.
---

**Contents**

[TOC]

### Compilation
- Java -server: Compiles with more aggressive optimizations and a larger set of compiler flags.
- Java -client: Compiles with less aggressive optimizations and a smaller set of compiler flags.

### Performance
- Java -server: Generally has better performance than java -client due to the more aggressive optimizations.

### Memory Usage
- Java -server: Uses more memory than java -client due to the larger set of compiler flags.

### Usage
- Java -server: Best used for applications that require higher performance and can tolerate higher memory usage.
- Java -client: Best used for applications that do not require higher performance and do not need to use a large amount of memory.
