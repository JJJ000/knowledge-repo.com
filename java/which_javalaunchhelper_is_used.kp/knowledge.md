---
title: The javalaunchhelper class is implemented in both the libjli.dylib and the libinstrument.dylib; however, it is not specified which of the two will be used
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The specific implementation of JavaLaunchHelper that is used is undefined.
---

**Contents**

[TOC]

## libinstrument.dylib
libinstrument.dylib is a dynamic library that is used to provide instrumentation and debugging capabilities for Java applications. It is a part of the Java Runtime Environment (JRE) and is installed with the JRE.

## JavaLaunchHelper
JavaLaunchHelper is a class that is used to launch Java applications. It is part of the Java Virtual Machine (JVM) and is included in the JRE. It is responsible for loading the class files and setting up the application environment.

## Which One is Used?
The actual implementation of JavaLaunchHelper is undefined and is determined by the JVM at runtime. The JVM will select the implementation of JavaLaunchHelper that is most suitable for the application being launched. This could be either the implementation in libinstrument.dylib or the implementation in the JVM.
