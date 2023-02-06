---
title: Setting up Java 7 on ubuntu
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `sudo apt-get install openjdk-7-jdk` to install Java 7 on Ubuntu.
---

**Contents**

[TOC]

# Section 1: Downloading Java 7
1. Add the webupd8team Java PPA repository to your system. Open a terminal window and enter the following command: 
```
sudo add-apt-repository ppa:webupd8team/java
```
2. Update your system's package index. Enter the following command in the terminal window: 
```
sudo apt-get update
```

# Section 2: Installing Java 7
1. Install the Oracle Java 7 JDK package. Enter the following command in the terminal window: 
```
sudo apt-get install oracle-java7-installer
```
2. Accept the Oracle license agreement. Select the "Yes" option when prompted.

# Section 3: Setting the Default Version of Java
1. Set the default version of Java to Java 7. Enter the following command in the terminal window: 
```
sudo update-alternatives --config java
```
2. Select the Oracle Java 7 JDK from the list of available versions. Enter the corresponding number and press Enter.

# Section 4: Verifying the Installation
1. Verify that Java 7 is installed correctly. Enter the following command in the terminal window: 
```
java -version
```
2. The output should show the version of Java installed, which should be Java 7.
