---
title: What is the intended use of meta-inf?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: META-INF is a directory in Java that contains files that provide information about the contents of a JAR file.
---

**Contents**

[TOC]

### Overview
META-INF is a directory that contains metadata about a Java archive (JAR) file. It is typically located at the root of a JAR file and contains a file called MANIFEST.MF.

### Manifest File
The MANIFEST.MF file contains information about the JAR file, such as the main class, version, and other related information. This information is used by the Java Virtual Machine (JVM) to properly run the JAR file.

### Security
META-INF is also used to store security certificates and signature files. These are used to ensure the integrity of the JAR file and prevent malicious tampering.

### Other Uses
META-INF can also be used to store additional information about the JAR file, such as license information and other metadata.
