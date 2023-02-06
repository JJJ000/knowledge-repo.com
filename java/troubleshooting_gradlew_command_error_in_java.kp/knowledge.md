---
title: What is the issue with running the 'gradlew' command?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: `gradlew` is a wrapper script for the Gradle build tool, so it must be installed in order to be used.
---

**Contents**

[TOC]

# Introduction
Gradle is a build automation tool used to compile, package, and deploy applications written in Java, C++, Python, and other languages. The gradlew command is a wrapper script that invokes the Gradle build system.

# Symptoms
When attempting to use the gradlew command in a Java project, the following error may be encountered:

`-bash: gradlew: command not found`

# Causes
This error can be caused by a few different issues:

- The gradlew script is not present in the project directory.
- The project is missing the Gradle wrapper configuration files.
- The PATH environment variable is not configured correctly.

# Resolution
1. Check if the gradlew script is present in the project directory. If it is not, download the Gradle wrapper configuration files from the Gradle website.

2. Check the PATH environment variable to make sure it is configured correctly.

3. If the issue persists, try reinstalling Gradle.
