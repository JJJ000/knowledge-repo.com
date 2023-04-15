---
title: Classes that do not contain instance members in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, a static class is a class that cannot be instantiated and is only used to hold static members.
---

**Contents**

[TOC]

### Definition
A static class in Java is a class that can only contain static members. It cannot be instantiated, and it can only contain static methods and static variables.

### Benefits
1. Static classes are more efficient since they do not need to be instantiated.
2. They can be used to store utility methods that are used throughout the program.
3. They can be used to create a namespace for related classes.

### Drawbacks
1. Since static classes cannot be instantiated, they cannot have any state associated with them.
2. They cannot be used as a base class for other classes.
3. They cannot be extended or have any subclasses.
