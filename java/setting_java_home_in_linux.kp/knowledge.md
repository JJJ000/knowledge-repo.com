---
title: How to configure java_home in linux for all users
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The JAVA\_HOME environment variable should be set in the /etc/environment file.
---

**Contents**

[TOC]

# Section 1: Finding the Java Home Path

1. Open a terminal window and type the following command:
```sh
$ sudo update-alternatives --config java
```
2. This command will list all the installed Java versions on your system. Note down the path of the Java version you want to set as JAVA_HOME.

# Section 2: Setting the Environment Variable

1. Open the .bashrc file in a text editor.
```sh
$ sudo nano ~/.bashrc
```
2. Add the following line to the end of the file, replacing the path with the one you noted down in the previous step.
```sh
export JAVA_HOME=/path/to/java
```
3. Save and close the file.

# Section 3: Source the .bashrc File

1. Source the .bashrc file to apply the changes.
```sh
$ source ~/.bashrc
```

# Section 4: Verifying the Changes

1. Check if the JAVA_HOME environment variable is set correctly.
```sh
$ echo $JAVA_HOME
```
2. The output should be the path to the Java version you set.
