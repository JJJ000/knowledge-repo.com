---
title: What is the process for transforming a kotlin source file into a Java source file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert a Kotlin source file to a Java source file, use the `Kotlin to Java` converter tool.
---

**Contents**

[TOC]

### Install Necessary Software

In order to convert a Kotlin source file to a Java source file, you will need to install the Kotlin Compiler. This can be done by downloading the latest version of the Kotlin compiler from the [official website](https://kotlinlang.org/docs/tutorials/command-line.html).

### Compile the Kotlin Source File

Once the Kotlin Compiler has been installed, you can compile the Kotlin source file using the command line. To do this, open a command prompt window and navigate to the directory containing the Kotlin source file. Then, enter the command `kotlinc <filename>.kt -include-runtime -d <filename>.jar`. This will create a Java archive (JAR) file that contains the compiled Kotlin source file.

### Decompile the JAR File

In order to convert the Kotlin source file to a Java source file, you will need to decompile the JAR file created in the previous step. This can be done using a tool such as JADX or JD-GUI. Once the JAR file has been decompiled, you will be able to view the Java source code of the Kotlin source file.

### Copy the Java Source Code

The last step is to copy the Java source code from the decompiled JAR file and save it as a Java source file. Once this is done, the Kotlin source file will have been successfully converted to a Java source file.
