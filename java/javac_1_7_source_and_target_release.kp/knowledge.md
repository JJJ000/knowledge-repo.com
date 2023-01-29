---
title: The source code for Java version 1.7 must be compiled with a target release of version 1.7
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, javac requires that the source and target releases be the same in order to compile a program.
---

**Contents**

[TOC]

### Introduction
Java is a popular programming language used to create a wide variety of applications and software. The Java compiler (javac) is used to compile Java source code into bytecode that can be executed on a Java Virtual Machine (JVM). One of the requirements for javac is that the source code and target code must be compatible.

### Source Release 1.7
Source release 1.7 is the version of Java used to create the source code. This version of Java contains the language features and APIs available in the 1.7 release of Java.

### Target Release 1.7
Target release 1.7 is the version of Java used to execute the compiled bytecode. This version of Java contains the language features and APIs available in the 1.7 release of Java.

### Does javac Require Source and Target Release 1.7?
Yes, javac requires that the source code and target code are both compatible with the 1.7 release of Java. If the source code is written in a later version of Java than the target code, javac will not be able to compile the source code.
