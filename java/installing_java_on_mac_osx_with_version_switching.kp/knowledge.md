---
title: What is the process for setting up Java on mac osx so that I can switch between different versions?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can install Java on Mac OSX by using a version manager such as jEnv or jabba.
---

**Contents**

[TOC]

### Install Homebrew
Homebrew is a package manager for macOS that allows you to install and manage software from the command line. 

To install Homebrew, open the terminal and run the following command:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

### Install Java
Once Homebrew is installed, you can use it to install the latest version of Java. To do this, run the following command in the terminal:

`brew cask install java`

### Switch Java Version
To switch between different versions of Java, you can use the `brew switch` command. For example, to switch to Java 8, run the following command:

`brew switch java 8.0.0`

### Verify Java Version
To verify the current version of Java, run the following command:

`java -version`
