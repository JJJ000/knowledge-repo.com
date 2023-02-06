---
title: What is the distinction between java_options, java_tool_options and java_opts?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: \_JAVA\_OPTIONS is used to set JVM-wide options, JAVA\_TOOL\_OPTIONS is used to set options for the Java launcher, and JAVA\_OPTS is used to set options for Java applications.
---

**Contents**

[TOC]

# JAVA_OPTIONS
JAVA_OPTIONS is an environment variable that can be used to set Java command-line options. These options are used to customize the Java Virtual Machine (JVM) and can be used to set parameters such as the initial and maximum heap size.

# JAVA_TOOL_OPTIONS
JAVA_TOOL_OPTIONS is an environment variable that can be used to pass additional options to the Java compiler and other tools such as javac, javadoc, and jar. These options can be used to customize the behavior of the tools and can be used to set parameters such as the source and target version of the Java compiler.

# JAVA_OPTS
JAVA_OPTS is an alias for JAVA_OPTIONS. It is used to set Java command-line options and can be used to customize the JVM.
