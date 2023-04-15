---
title: System configurations of Java and environmental variables
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: System properties are set by the Java Virtual Machine (JVM) when it starts and can be read by Java applications, while environment variables are set by the operating system and can be read by any application.
---

**Contents**

[TOC]

### System Properties

System properties are a set of key-value pairs that provide configuration settings for the Java Virtual Machine (JVM) and the Java application. These properties are set either on the command line when starting the JVM or by setting them directly in the system. They can be accessed through the System.getProperty() method.

### Environment Variables

Environment variables are a set of key-value pairs that provide configuration settings for the operating system and the applications running in it. They are set either in the operating system or in the application itself. They can be accessed through the System.getenv() method.
