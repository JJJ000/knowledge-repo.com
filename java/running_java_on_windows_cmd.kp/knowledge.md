---
title: What is the process for executing a Java program from the command line in windows?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To run a Java program from the command line on Windows, type `java <classname>` in the command prompt.
---

**Contents**

[TOC]

# Step 1: Compile the Program 

In order to run a Java program from the command line on Windows, the program must first be compiled. To do this, open a command prompt window (by typing "cmd" into the search bar) and navigate to the directory containing the program's source code. Then type the command `javac <filename>.java` to compile the program, where `<filename>` is replaced with the name of the source code file.

# Step 2: Create a Manifest File 

If the program requires external libraries, create a manifest file in the same directory as the source code. The manifest file should be named `manifest.txt` and should contain the line `Class-Path: <library_name>.jar`, where `<library_name>` is replaced with the name of the library.

# Step 3: Create a JAR File 

Next, create a JAR file that contains the program's compiled class files and the manifest file. To do this, type the command `jar cvfm <jar_name>.jar manifest.txt *.class` into the command prompt window. This will create a JAR file with the name `<jar_name>` and the suffix `.jar`, where `<jar_name>` is replaced with the desired name for the JAR file.

# Step 4: Run the Program 

Finally, to run the program, type the command `java -jar <jar_name>.jar` into the command prompt window, where `<jar_name>` is replaced with the name of the JAR file created in the previous step. This will execute the program.
