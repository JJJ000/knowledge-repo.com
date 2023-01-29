---
title: The javax.xml.bind package is not available in Java 11
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The javax.xml.bind package is not available in Java 11, as it has been removed from the Java SE platform.
---

**Contents**

[TOC]

### Introduction

Java 11 does not include the javax.xml.bind package, which was part of Java 8 and earlier versions.

### Reasons for Removal

The javax.xml.bind package was removed from Java 11 in order to reduce the size of the Java SE Platform and to simplify the development and maintenance of the Java SE Platform.

### Alternatives

The Java 11 platform includes the javax.xml.transform package, which provides basic support for XML processing, including XML parsing and transformation. Additionally, Java 11 includes the JAXB API, which provides a set of APIs for the Java platform that enable developers to marshal Java objects into XML and unmarshal XML back into Java objects.

### Conclusion

The removal of the javax.xml.bind package from Java 11 was done to reduce the size of the Java SE Platform and simplify its development and maintenance. Alternatives, such as the javax.xml.transform and JAXB APIs, are available to developers for XML processing.
