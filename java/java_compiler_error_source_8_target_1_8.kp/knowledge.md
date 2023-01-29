---
title: The Java compiler is unable to compile the source code because it was written in Java 8, which requires a target release of 1.8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The javac compiler must be set to the same version as the source code in order to compile successfully.
---

**Contents**

[TOC]

### What is the Error?
The error "source release 8 requires target release 1.8" is thrown when a Java program is compiled with a version of the Java compiler that is incompatible with the version of the Java language used in the program.

### What Causes the Error?
This error occurs when the Java compiler used to compile the program is not compatible with the version of the Java language used in the program. For example, if the program uses Java 8 syntax and the compiler is configured to use Java 7, the error will be thrown.

### How to Resolve the Error?
To resolve this error, the Java compiler must be configured to use the same version of the Java language as the program. This can be done by setting the appropriate compiler options in the build file or by using a compatible version of the Java compiler.

### Conclusion
The error "source release 8 requires target release 1.8" occurs when a Java program is compiled with a version of the Java compiler that is incompatible with the version of the Java language used in the program. To resolve this error, the Java compiler must be configured to use the same version of the Java language as the program.
