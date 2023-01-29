---
title: Unfortunately, it is not possible to have both non-gradle Java modules and android-gradle modules in the same project
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: No, it is not possible to have non-Gradle Java modules and Android-Gradle modules in one project.
---

**Contents**

[TOC]

### Overview
Unfortunately, it is not possible to have non-Gradle Java modules and Android-Gradle modules in one project. This is because the two systems are incompatible and cannot be integrated together. This article will explain why this is the case and provide alternatives for projects that require both Java and Android modules.

### Incompatibility
The main issue with having non-Gradle Java modules and Android-Gradle modules in one project is that the two systems are incompatible. Non-Gradle Java modules are built using the traditional Ant-based build system, while Android-Gradle modules are built using the Gradle-based build system. The two systems use different build scripts, different build tools, and different build configurations, making them incompatible.

### Alternatives
If a project requires both Java and Android modules, there are two main alternatives. The first is to use a single system for both Java and Android modules. This can be done by either using the Gradle-based build system for both, or by using the Ant-based build system for both. The second alternative is to use two separate projects, one for the Java modules and one for the Android modules. This allows the two systems to remain separate, while still allowing the two projects to communicate with each other.

### Conclusion
Unfortunately, it is not possible to have non-Gradle Java modules and Android-Gradle modules in one project. This is because the two systems are incompatible and cannot be integrated together. However, there are alternatives such as using a single system for both Java and Android modules, or using two separate projects.
