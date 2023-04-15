---
title: What is the process for converting dex files into Java source code?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a Java decompiler such as JD-GUI to decompile DEX into Java source code.
---

**Contents**

[TOC]

### Prerequisites

Before attempting to decompile a DEX file into Java source code, you must have the following prerequisites in place:

- JD-GUI (Java Decompiler): This is a graphical utility that allows you to view the source code of Java class files. It works with Java bytecode and DEX files, and can be downloaded from the official website.

- Dex2Jar: This is a tool that can convert a DEX file into a JAR file, which can then be opened with JD-GUI. It can be downloaded from the official website.

### Convert DEX to JAR

Once you have the necessary prerequisites in place, the next step is to convert the DEX file into a JAR file. To do this, use Dex2Jar to convert the DEX file into a JAR file.

### Open JAR with JD-GUI

Once the DEX file has been converted to a JAR file, you can then open the JAR file with JD-GUI. This will display the Java source code of the DEX file in a graphical user interface.

### Save Source Code

Finally, you can save the Java source code of the DEX file by clicking on the “Save All Sources” button in the JD-GUI window. This will save all of the Java source code to the specified directory.
