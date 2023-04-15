---
title: What is the platform-specific new line character?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use System.getProperty(`line.separator`) to get the platform-dependent new line character in Java.
---

**Contents**

[TOC]

### Using System.lineSeparator()
System.lineSeparator() is a static method of the System class which returns the platform-dependent line separator character as a string. It is the recommended way to get the line separator character in Java.

### Using System Properties
System properties can also be used to get the platform-dependent line separator character. The line separator character is stored in the system property line.separator.

### Using "\n"
The character "\n" can also be used to get the platform-dependent line separator character. However, this is not the recommended way since it is not platform-independent.

### Using System.getProperty()
System.getProperty() method can also be used to get the platform-dependent line separator character. It takes the system property line.separator as an argument and returns the line separator character as a string.
