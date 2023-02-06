---
title: Which version of javac was used to create my jar?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The version of javac used to build the jar can be determined by running the `jar -xf` command.
---

**Contents**

[TOC]

# Version Identification

To identify the version of javac that built your jar, you can use the `javap` command. This command prints out the bytecode that is contained in the .class files in your jar.

# Running the Command

To run the command, open a terminal window and navigate to the directory where your jar is located. Then, type the command: 

`javap -verbose -classpath <jar-name>.jar <class-name>.class`

Replace `<jar-name>` with the name of your jar file, and `<class-name>` with the name of the class you want to inspect.

# Output

The output of the command will include the version of javac that built your jar. The version number will be in the form `major.minor.patch`. For example, `1.8.0_202` indicates a javac version of 1.8.0 with a patch level of 202.
