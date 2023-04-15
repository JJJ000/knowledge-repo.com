---
title: The installation of android-sdk was unsuccessful due to a "java.lang.noclassdeffounderror javax/xml/bind/annotation/xmlschema" error
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Java version being used may be too old to support the javax.xml.bind.annotation.XmlSchema class.
---

**Contents**

[TOC]

### Overview

The java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema error occurs when the Java Virtual Machine (JVM) attempts to load a class that is not available in the classpath. In this case, it is likely that the class XmlSchema is missing from the classpath when attempting to install the android-sdk. 

### Causes

The most common cause of this error is that the required JAR file is not present in the classpath. This could be due to the JAR file being missing from the installation package, or not being included in the classpath during the installation process. Additionally, the error could be caused by an outdated version of the JAR file or a corrupted version of the JAR file. 

### Solutions

The first step to resolving this issue is to ensure that the correct version of the JAR file is present in the classpath. If the correct version is not present, it should be downloaded and added to the classpath. Additionally, it is recommended to check the integrity of the JAR file to ensure that it is not corrupted. If the JAR file is corrupted, it should be replaced with a valid version. 

Finally, it is important to ensure that the JAR file is included in the classpath when installing the android-sdk. This can be done by manually adding the JAR file to the classpath or by using a tool such as Maven or Ant to automate the process. 

### Conclusion

The java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema error can be caused by a missing or corrupted JAR file. To resolve this issue, it is important to ensure that the correct version of the JAR file is present in the classpath and that it is included in the classpath when installing the android-sdk. Additionally, it is recommended to check the integrity of the JAR file to ensure that it is not corrupted.
