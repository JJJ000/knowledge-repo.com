---
title: What is the difference between "mvn clean package" and "mvn clean install"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: `mvn clean package` creates a jar file of the project, while `mvn clean install` installs the jar file into the local repository.
---

**Contents**

[TOC]

#Overview
Maven is a build automation tool used primarily for Java projects. The two commands "mvn clean package" and "mvn clean install" are used to build and deploy Java projects. 

#mvn clean package
The command "mvn clean package" is used to compile and package the source code into a distributable format such as a JAR or WAR file. This command will create the compiled code in the target directory and package it into a distributable format.

#mvn clean install
The command "mvn clean install" is used to compile, package, and install the project in the local repository. This command will compile the source code, package it into a distributable format, and then install it in the local repository for use by other projects.

#Differences
The main difference between "mvn clean package" and "mvn clean install" is that the latter command will install the project in the local repository while the former will only compile and package the code. Another difference is that the "mvn clean package" command is used to create distributable artifacts while the "mvn clean install" command is used to install the project in the local repository.
