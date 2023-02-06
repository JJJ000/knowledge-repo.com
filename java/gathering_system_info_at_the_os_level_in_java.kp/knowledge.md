---
title: Retrieve operating system-level details
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The java.lang.System class provides methods for getting system information such as the current time, the current user, the system properties, and the environment variables.
---

**Contents**

[TOC]

## System Properties

Java provides a class called `System` containing a set of system properties. These properties provide information about the current operating system, such as the name, version, architecture, and other details. This information can be accessed via the `System.getProperties()` method.

## Operating System MXBean

The `OperatingSystemMXBean` interface provides access to OS-level information such as the number of processors, system load average, and system uptime. This information can be accessed via the `ManagementFactory.getOperatingSystemMXBean()` method.

## Runtime

The `Runtime` class provides access to the underlying operating system. This class provides methods to get the name and version of the operating system, as well as the total amount of memory available to the JVM.

## Native Libraries

Finally, native libraries such as JNI (Java Native Interface) can be used to access OS-level information. This approach requires the use of platform-specific code and is not recommended for most use cases.
