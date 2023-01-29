---
title: What steps are needed to modify the default Java version on a mac computer?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To set or change the default Java (JDK) version on macOS, use the command line tool `/usr/libexec/java\_home -v [version] -s` to set the desired version.
---

**Contents**

[TOC]

### Check Installed Java Versions

To check which Java versions are installed on your macOS, open the Terminal app and enter the following command:

`/usr/libexec/java_home -V`

This will list all the installed Java versions.

### Set Default Java Version

To set the default Java version, open the Terminal app and enter the following command:

`export JAVA_HOME=`/usr/libexec/java_home -v <version>

Replace <version> with the version number you want to set as the default.

### Verify Default Java Version

To verify that the default Java version has been set, open the Terminal app and enter the following command:

`echo $JAVA_HOME`

This will display the path to the default Java version.

### Set Default Java Version for Applications

To set the default Java version for applications, open the Terminal app and enter the following command:

`/usr/libexec/java_home -s <version>`

Replace <version> with the version number you want to set as the default.
