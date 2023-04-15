---
title: Avoid using wildcard imports when working with intellij
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is best practice to avoid wildcard imports in Java, as they can lead to ambiguity and confusion.
---

**Contents**

[TOC]

1. **Why Wildcard Imports Are Not Recommended**
Wildcard imports are not recommended because they can lead to confusing code. When a wildcard import is used, all classes from the imported package are imported into the current namespace. This can lead to name collisions, where two classes with the same name are imported from different packages. This can lead to unexpected behavior and make code difficult to debug.

2. **Clarity and Readability**
Wildcard imports can make code difficult to read and understand. When a wildcard import is used, it is not immediately clear which classes are imported and from which package they are imported. This can make it difficult to determine which classes are being used and how they interact with each other.

3. **Performance**
Wildcard imports can also lead to performance issues. When a wildcard import is used, all classes from the imported package are loaded into memory, even if they are not used. This can lead to unnecessary memory usage and slower execution times.

4. **Best Practices**
It is best practice to avoid wildcard imports in Java. Instead, import only the classes that are needed for a specific task. This will help ensure that code is clear and easy to understand, and will help to avoid potential memory and performance issues.
