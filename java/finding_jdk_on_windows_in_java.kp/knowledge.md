---
title: Where is the jdk located on my windows computer?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can find the JDK installation directory by running the `where javac` command in the command line.
---

**Contents**

[TOC]

### Using Environment Variables

1. Open the Control Panel.
2. Select System and Security.
3. Select System.
4. Select Advanced System Settings.
5. Select Environment Variables.
6. In the System Variables list, look for the JAVA_HOME variable.
7. The value of the JAVA_HOME variable is the JDK installation directory.

### Using Command Prompt

1. Open the Command Prompt.
2. Type the command `java -version` and press Enter.
3. The output will display the version of the JDK installed and the installation directory.
