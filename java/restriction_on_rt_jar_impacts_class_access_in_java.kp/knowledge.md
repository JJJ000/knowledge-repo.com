---
title: What are the limitations on using the rt.jar library that are affecting access to the class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Classes that require rt.jar cannot be accessed if the library is restricted.
---

**Contents**

[TOC]

### What is rt.jar?
rt.jar is a Java Archive (JAR) file that contains most of the core classes of the Java Standard Edition (SE) platform. It is part of the Java Runtime Environment (JRE) and contains the Java Virtual Machine (JVM) implementation, along with the class libraries used by the JVM.

### Restrictions on rt.jar
Due to the sensitive nature of the code contained in rt.jar, there are certain restrictions on its use. These restrictions are imposed by the Java Runtime Environment (JRE) and include:

- rt.jar must be included in the classpath of any application that uses it.
- The code in rt.jar cannot be modified or redistributed.
- rt.jar must be used in accordance with the terms of the Java SE license.

### Impact on Classes
Since rt.jar is a core component of the JRE, any class that depends on it will be restricted in some way. This could include restrictions on the use of certain classes or methods, or even the inability to use certain classes or methods at all.

### Conclusion
In conclusion, the restriction on rt.jar can have a significant impact on the classes that depend on it. Developers should be aware of these restrictions and ensure that their applications comply with the terms of the Java SE license.
