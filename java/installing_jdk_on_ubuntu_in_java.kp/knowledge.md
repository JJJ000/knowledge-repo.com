---
title: What is the process for setting up the jdk on ubuntu linux?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run the command `sudo apt-get install default-jdk` to install the JDK on Ubuntu Linux.
---

**Contents**

[TOC]

### Download the JDK
1. Download the JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Select the version of the JDK that is compatible with your Ubuntu version.
3. Download the tar.gz file for the JDK.

### Install the JDK
1. Open the terminal and navigate to the directory where the tar.gz file was downloaded.
2. Extract the JDK files using the command `tar xvf <jdk-file-name>.tar.gz`.
3. Move the extracted JDK folder to the `/usr/lib/jvm` directory using the command `sudo mv <jdk-file-name> /usr/lib/jvm`.

### Set Java Environment Variables
1. Set the `JAVA_HOME` environment variable using the command `export JAVA_HOME=/usr/lib/jvm/<jdk-file-name>`.
2. Set the `PATH` environment variable using the command `export PATH=$PATH:$JAVA_HOME/bin`.

### Verify the Installation
1. Verify that the JDK is installed correctly by running the command `java -version`.
2. The output should display the version of the JDK that was installed.
