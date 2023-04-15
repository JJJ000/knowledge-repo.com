---
title: What do the terms 'young,' 'old,' and 'permanent' mean in relation to the Java heap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The young generation is where most new objects are allocated, the old generation is where longer-lived objects are moved to after surviving the young generation, and the permanent generation contains metadata required by the JVM to describe the classes and methods used in the application.
---

**Contents**

[TOC]

### Young Generation
The young generation is the part of the heap where objects that have been recently created are stored. This generation is further divided into three parts: Eden, Survivor 0, and Survivor 1. When an object is created, it is allocated in the Eden space. When the Eden space becomes full, a minor garbage collection is triggered, where the live objects are moved to Survivor 0. When Survivor 0 becomes full, the live objects are moved to Survivor 1. The objects that remain in the Eden and Survivor spaces after the minor garbage collection are then eligible for garbage collection.

### Old Generation
The old generation is the part of the heap where objects that have been around for some time are stored. This generation is also subject to garbage collection, but it occurs less often than the minor garbage collection in the young generation. During an old generation garbage collection, the live objects are compacted and moved to a different part of the heap. The objects that remain are then eligible for garbage collection.

### Permanent Generation
The permanent generation is the part of the heap where class and method objects are stored. This generation is not subject to garbage collection, and the objects stored there are not eligible for garbage collection.
