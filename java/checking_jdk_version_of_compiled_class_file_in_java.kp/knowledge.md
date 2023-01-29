---
title: What is the jdk version used to compile a .class file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the javap command to check the jdk version used to compile a .class file in Java.
---

**Contents**

[TOC]

### Using javap

javap is a Java class file disassembler that comes with the JDK. It can be used to print out the bytecode instructions contained in a .class file.

### Prerequisites

* JDK installed on your machine

### Steps

1. Open a command prompt and navigate to the directory containing the .class file.
2. Execute the following command: 
    ```java
    javap -verbose <class file name>
    ```
3. Look for the following line in the output:
    ```java
    major version: <version>
    ```
4. The version number indicated is the JDK version used to compile the .class file.
