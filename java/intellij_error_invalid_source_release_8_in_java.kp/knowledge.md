---
title: This error message indicates that intellij is not compatible with Java 8 and cannot use it as a source release
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It means that the project is using a version of Java that is not supported by Intellij.
---

**Contents**

[TOC]

### Overview 
The error "invalid source release: 8" in Intellij is an indication that the version of Java being used is not compatible with the Intellij version being used. This error is usually encountered when attempting to compile a project in Intellij using a version of Java that is not supported by the current version of Intellij.

### Causes
This error is usually caused by attempting to use an older version of Java with an updated version of Intellij. For instance, if Intellij is updated to the latest version but the Java version is still an older one, this error can occur.

### Solutions
The most straightforward solution is to update the version of Java being used to one that is compatible with the current version of Intellij. If this is not possible, then a workaround might be to use an older version of Intellij that is compatible with the version of Java being used.
