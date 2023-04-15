---
title: What steps can be taken to resolve the Java.lang.UnsupportedClassVersionError `unsupported major.minor version` error?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Upgrade the version of Java being used to one that is compatible with the class version.
---

**Contents**

[TOC]

### 1. Check JVM Version

The first step to fixing the `java.lang.UnsupportedClassVersionError` is to check the version of the Java Virtual Machine (JVM) that is installed. To do this, run the `java -version` command in your terminal. This will output the installed version of the JVM.

### 2. Check Compiled Class Version

The next step is to check the version of the compiled class that is causing the error. To do this, run the `javap -verbose <classname>` command in your terminal, where `<classname>` is the name of the compiled class that is causing the error. This will output information about the compiled class, including the version of the Java compiler that was used to compile the class.

### 3. Update JVM Version

If the version of the JVM is lower than the version of the compiled class, then you need to update the JVM to the same version as the compiled class. To do this, download and install the appropriate version of the JVM from the Java website.

### 4. Recompile Class

If the version of the JVM is higher than the version of the compiled class, then you need to recompile the class using the same version of the Java compiler that was used to compile the class. To do this, download and install the appropriate version of the Java compiler from the Java website. Once the Java compiler is installed, use it to recompile the class.
