---
title: What is the process for establishing a java_home environment variable on windows 7?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Set the JAVA\_HOME environment variable to the path of your Java installation.
---

**Contents**

[TOC]

### Finding the Java Home Path
1. Open the Windows Control Panel.
2. Select the System icon.
3. Click on the Advanced system settings link.
4. Click on the Environment Variables button.
5. Under System Variables, select the Path variable and click Edit.
6. Copy the path of the Java installation directory.

### Setting the Java Home Path
1. Open the System Properties window.
2. Click on the Advanced tab.
3. Click on the Environment Variables button.
4. Under System Variables, click New.
5. Enter `JAVA_HOME` in the Variable name field.
6. Enter the path of the Java installation directory in the Variable value field.
7. Click OK.

### Verifying the Java Home Path
1. Open the Command Prompt.
2. Type `echo %JAVA_HOME%` and press Enter.
3. The path of the Java installation directory should be displayed.

### Setting the Path Variable
1. Open the System Properties window.
2. Click on the Advanced tab.
3. Click on the Environment Variables button.
4. Under System Variables, select the Path variable and click Edit.
5. Append the `%JAVA_HOME%\bin` path to the end of the Variable value field.
6. Click OK.
