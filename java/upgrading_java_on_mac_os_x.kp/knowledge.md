---
title: I installed Java 7 on my mac os x, but the terminal is still using version 6
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Run the command `java -version` to check which version of Java is being used, then use the command `export JAVA\_HOME=<path/to/java/7>` to set the JAVA\_HOME environment variable to the path of the Java 7 installation.
---

**Contents**

[TOC]

### Uninstall Java 6
1. Open **Terminal** and type the following command to check the version of Java installed on your Mac: 
`java -version`
2. If the version is Java 6, type the following command to uninstall it: 
`sudo rm -fr /System/Library/Frameworks/JavaVM.framework/Versions/1.6`
3. Enter your Mac password when prompted and press `Enter` to complete the uninstallation process.

### Install Java 7
1. Download the latest version of Java 7 from the [Oracle website](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html).
2. Once the download is complete, open the **.dmg** file and double-click the **.pkg** file to start the installation.
3. Follow the on-screen instructions and complete the installation process.

### Update Java Version
1. Open **Terminal** and type the following command to check the version of Java installed on your Mac: 
`java -version`
2. If the version is Java 7, type the following command to update the default version of Java used by the Terminal: 
`export JAVA_HOME=`/Library/Java/JavaVirtualMachines/jdk1.7.0_79.jdk/Contents/Home``
3. Press `Enter` to update the default version of Java used by the Terminal.
