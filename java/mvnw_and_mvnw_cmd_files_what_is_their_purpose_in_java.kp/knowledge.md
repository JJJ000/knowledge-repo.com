---
title: What do the mvnw and mvnw.cmd files do?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The mvnw and mvnw.cmd files are used to run the Maven build tool in a platform-independent manner.
---

**Contents**

[TOC]

### Overview
Mvnw and mvnw.cmd are files used to manage a project's build, testing, and deployment using the Maven build automation tool. These files are used to simplify the process of running Maven commands and are especially useful for projects that use multiple operating systems.

### Mvnw
Mvnw is a shell script that is used to run Maven commands on Unix-based operating systems such as Linux and macOS. It is written in the Bash scripting language and is designed to be platform-independent.

### Mvnw.cmd
Mvnw.cmd is a Windows batch file that is used to run Maven commands on Windows operating systems. It is written in the Windows batch scripting language and is designed to be platform-specific.

### Benefits
Using mvnw and mvnw.cmd files simplifies the process of running Maven commands. It eliminates the need to manually enter the same Maven command for different operating systems and allows developers to quickly and easily manage their project's build, testing, and deployment.
