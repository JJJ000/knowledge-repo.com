---
title: Tomcat server at localhost requires the use of several ports (8005, 8080, 8009), but they are already occupied
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, these ports are already in use by the Java Runtime Environment (JRE).
---

**Contents**

[TOC]

## Yes

Tomcat Server requires several ports to operate. These ports include 8005, 8080, and 8009. All of these ports are already in use by the Java platform. Java uses these ports for its various services, such as RMI, JNDI, and JMX.

## Why

The ports required by Tomcat Server are used by Java to facilitate communication between the different components of the platform. For example, port 8005 is used by the Java Virtual Machine (JVM) to perform remote method invocation (RMI). Port 8080 is used by Java Naming and Directory Interface (JNDI) to look up services and objects in the network. And port 8009 is used by Java Management Extensions (JMX) to manage and monitor the application.

## How

These ports are configured by the Java platform at startup. The ports can be changed by editing the `conf/server.xml` file in the Tomcat installation directory. The ports can also be changed using the `setenv.sh` (for Linux/macOS) or `setenv.bat` (for Windows) script. This script is located in the `bin` directory of the Tomcat installation.
