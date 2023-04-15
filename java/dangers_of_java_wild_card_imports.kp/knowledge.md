---
title: What are the drawbacks of using a wild card with a Java import statement?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using a wild card with a Java import statement can lead to confusion and errors due to conflicting class names.
---

**Contents**

[TOC]

### Unnecessary Imports
Using a wild card with a Java import statement is bad because it imports all the classes from the package, even those that are not used in the program. This can lead to unnecessary imports, which can increase the size of the program and slow down its execution time. 

### Conflicts
Using a wild card with a Java import statement can also cause conflicts between different classes with the same name. For example, if two packages contain classes with the same name, the wild card import statement will import both classes, leading to conflicts and errors. 

### Harder to Read
Using a wild card with a Java import statement can also make the program harder to read. This is because the wild card import statement imports all classes from the package, making it difficult to tell which classes are actually being used in the program. 

### Security Issues
Finally, using a wild card with a Java import statement can lead to security issues. This is because the wild card import statement imports all classes from the package, including potentially malicious classes that may contain malicious code.
