---
title: The Maven surefire plugin was unable to locate the forkedbooter class
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Maven surefire cannot find ForkedBooter class because it is not part of the standard Java class library.
---

**Contents**

[TOC]

# Introduction
Maven Surefire is a plugin used to execute unit tests in a project. It is part of the Apache Maven project and is used to run unit tests written in the JUnit, TestNG, and other testing frameworks.

# Problem
Maven Surefire may not be able to find the ForkedBooter class when running tests in Java. This can be caused by a variety of issues, such as incorrect configuration or missing dependencies.

# Solution
The first step is to ensure that the surefire-plugin is properly configured in the project's pom.xml. The surefire-plugin should have the correct version of the forked-booter dependency declared. Additionally, the version of the forked-booter dependency should match the version of the surefire-plugin. 

Next, it is important to make sure that all of the required dependencies are present in the project's classpath. This includes the surefire-booter and the forked-booter dependencies. If any of the dependencies are missing, they should be added to the project's pom.xml.

# Conclusion
Maven Surefire may not be able to find the ForkedBooter class when running tests in Java. To resolve this issue, it is important to make sure that the surefire-plugin is properly configured and all of the required dependencies are present in the project's classpath.
