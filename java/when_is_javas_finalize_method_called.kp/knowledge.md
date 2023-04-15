---
title: What is the timing of the invocation of the finalize() method in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The finalize() method is called by the garbage collector when an object is no longer being used or referenced.
---

**Contents**

[TOC]

### When the Garbage Collector Runs
The finalize() method is called when the garbage collector runs and determines that the object is no longer reachable.

### When the Object is Finalized
The finalize() method is called when the object is finalized, which is when the garbage collector runs and determines that the object is no longer reachable.

### When the Program Ends
The finalize() method is also called when the program ends, as this is the last chance for the garbage collector to clean up any objects that are no longer reachable.

### When the Object is Destroyed
The finalize() method is also called when the object is destroyed, which is when the garbage collector runs and determines that the object is no longer reachable.
