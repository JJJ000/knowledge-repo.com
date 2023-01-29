---
title: Maven is not functioning properly when javadoc tags are incomplete in Java 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Maven will not build if Javadoc tags are incomplete in Java 8.
---

**Contents**

[TOC]

### Problem
Maven is not working in Java 8 when Javadoc tags are incomplete.

### Causes
The main cause of this issue is that Java 8 requires all Javadoc tags to be complete in order for Maven to be able to build the project. If any of the tags are missing or incomplete, then Maven will fail to build the project.

### Solutions
1. Ensure that all Javadoc tags are complete and correct before attempting to build the project with Maven.
2. Use an automated tool to check for missing or incomplete Javadoc tags.
3. Use a plugin such as the Maven Javadoc Plugin to generate Javadoc tags automatically.
4. Use a tool such as the Maven Javadoc Checker to check for missing or incomplete Javadoc tags.
