---
title: How can I configure the environment variables for Java in windows?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Set the JAVA\_HOME environment variable to the path of the Java installation directory.
---

**Contents**

[TOC]

##### Setting Environment Variables
1. Open the Control Panel.
2. Go to System and Security > System > Advanced system settings > Environment Variables.
3. Click New under the User variables section.
4. Enter the Variable name as `JAVA_HOME` and Variable value as the installation path of the Java Development Kit (JDK).
5. Click OK.

##### Setting Path Variable
1. Select the Path variable under the System variables section.
2. Click Edit.
3. Enter the path of the Java bin folder.
4. Click OK.

##### Testing the Installation
1. Open Command Prompt.
2. Enter `java -version` and press Enter to check the version of Java installed.
3. Enter `javac -version` and press Enter to check if the Java compiler is working.
