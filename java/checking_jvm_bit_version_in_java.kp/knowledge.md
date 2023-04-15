---
title: What is the method of determining whether a program is running in a 64-bit or 32-bit jvm?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `System.getProperty(`sun.arch.data.model`)` method to get the JVM bitness.
---

**Contents**

[TOC]

1. Use System Properties
------------------------
The easiest way to determine if you are running in a 32-bit or 64-bit JVM is to use the system properties. You can use the following code to get the system property "sun.arch.data.model":

```
String arch = System.getProperty("sun.arch.data.model");
if (arch.equals("32")) {
    // 32-bit JVM
} else if (arch.equals("64")) {
    // 64-bit JVM
}
```

2. Use RuntimeMXBean
--------------------
Another way to determine if you are running in a 32-bit or 64-bit JVM is to use the RuntimeMXBean. You can use the following code to get the system property "sun.arch.data.model":

```
RuntimeMXBean runtimeMxBean = ManagementFactory.getRuntimeMXBean();
String arch = runtimeMxBean.getInputArguments().get(0);
if (arch.equals("-d32")) {
    // 32-bit JVM
} else if (arch.equals("-d64")) {
    // 64-bit JVM
}
```

3. Use Operating System
-----------------------
You can also use the operating system to determine if you are running in a 32-bit or 64-bit JVM. You can use the following code to get the system property "os.arch":

```
String arch = System.getProperty("os.arch");
if (arch.equals("x86") || arch.equals("i386") || arch.equals("i686")) {
    // 32-bit JVM
} else if (arch.equals("amd64") || arch.equals("x86_64")) {
    // 64-bit JVM
}
```

4. Use Java Version
-------------------
You can also use the Java version to determine if you are running in a 32-bit or 64-bit JVM. You can use the following code to get the system property "java.version":

```
String version = System.getProperty("java.version");
if (version.contains("_32")) {
    // 32-bit JVM
} else if (version.contains("_64")) {
    // 64-bit JVM
}
```
