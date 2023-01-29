---
title: Interpreted languages versus compiled languages
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Java is a compiled language, meaning the source code is converted into bytecode which is then interpreted by the Java Virtual Machine.
---

**Contents**

[TOC]

### Compiled Languages

A compiled language is a programming language whose implementations are typically compilers (translators that generate machine code from source code), and not interpreters (step-by-step executors of source code, where no pre-runtime translation takes place).

Java is a compiled language, meaning that the source code is translated into bytecode, which is then executed by the Java Virtual Machine (JVM). The JVM is responsible for interpreting the bytecode and executing it on the underlying hardware.

### Interpreted Languages

An interpreted language is a programming language whose implementations are typically interpreters (step-by-step executors of source code, where no pre-runtime translation takes place).

Java is not an interpreted language, as the source code is not directly executed by the JVM. Instead, it is translated into bytecode, which is then executed by the JVM.

### Advantages of Compiled Languages

Compiled languages offer several advantages, including:

- Faster execution times, as the code is already translated into machine-readable language and does not have to be interpreted at runtime.

- Easier debugging, as errors can be identified and fixed before the program is executed.

- More efficient memory use, as the code is already in a compact form.

### Advantages of Interpreted Languages

Interpreted languages offer several advantages, including:

- Easier development, as the code can be written and tested quickly without the need for a compilation step.

- More flexibility, as the code can be modified while the program is running.

- Easier portability, as the code does not need to be recompiled for different platforms.
