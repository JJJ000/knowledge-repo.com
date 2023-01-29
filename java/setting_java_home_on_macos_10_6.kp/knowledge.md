---
title: How do I configure the java_home environment variable on macos x 10.6?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: JAVA\_HOME should be set to the path of the JDK installation directory.
---

**Contents**

[TOC]

### Find the Java Home Directory
1. Open a Terminal window.
2. Type the command `/usr/libexec/java_home -V`

### Set the JAVA_HOME Environment Variable
1. Type the command `export JAVA_HOME=`
2. Paste the output from the previous step after the equals sign.

### Verify the JAVA_HOME Environment Variable
1. Type the command `echo $JAVA_HOME`
2. Verify that the output matches the output from the previous step.

### Save the JAVA_HOME Environment Variable
1. Type the command `nano ~/.bash_profile`
2. Paste the command `export JAVA_HOME=` followed by the output from the first step into the file.
3. Save the file and exit.
