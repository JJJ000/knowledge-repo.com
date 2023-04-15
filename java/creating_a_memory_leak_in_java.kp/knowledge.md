---
title: What steps can I take to cause a memory leak in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: By creating objects that are never garbage collected, such as by storing references to them in static fields.
---

**Contents**

[TOC]

### Creating a Memory Leak
1. Create an object inside a loop that is never dereferenced.
2. Use a static reference to the object.
3. Keep the loop running indefinitely.

### Example
The following code creates a memory leak by creating an array of objects inside a loop, referencing them with a static field, and never dereferencing them:

```java
public class MemoryLeak {
  private static List<Object> list = new ArrayList<Object>();
 
  public static void main(String[] args) {
    while (true) {
      list.add(new Object());
    }
  }
}
```
