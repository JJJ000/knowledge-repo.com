---
title: What is the location of the jar file that is currently running?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the System.getProperty(`java.class.path`) method to get the path of a running JAR file in Java.
---

**Contents**

[TOC]

### Using Java's getProtectionDomain() Method

The `getProtectionDomain()` method of the `java.lang.Class` class can be used to get the path of a running JAR file in Java. This method returns a `java.security.ProtectionDomain` object that contains information about the origin of a class, including the code source and the signing certificates.

### Using the CodeSource

Once the `ProtectionDomain` object is obtained, the `getCodeSource()` method can be used to get the `java.security.CodeSource` object, which contains the path of the JAR file. The `getLocation()` method of the `CodeSource` object can then be used to get the `java.net.URL` object, which contains the path of the JAR file.

### Converting the URL to a String

The `URL` object can then be converted to a `String` using the `toExternalForm()` method. This will return the path of the JAR file as a `String`.

### Example

The following example shows how to get the path of a running JAR file in Java:

```java
Class<?> clazz = MyClass.class;
ProtectionDomain pd = clazz.getProtectionDomain();
CodeSource cs = pd.getCodeSource();
URL url = cs.getLocation();
String jarFilePath = url.toExternalForm();
System.out.println("Jar file path: " + jarFilePath);
```
