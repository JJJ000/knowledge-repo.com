---
title: I am unable to compile the project when using lombok in intellij idea
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Make sure that the Lombok plugin is enabled in IntelliJ IDEA.
---

**Contents**

[TOC]

# Solution

## Install Lombok Plugin

The first step in resolving this issue is to install the Lombok plugin in IntelliJ IDEA. The plugin can be found in the IntelliJ IDEA plugins repository. Once installed, the plugin will enable the IDE to recognize Lombok annotations and compile the project accordingly.

## Enable Annotation Processing

The next step is to enable annotation processing in IntelliJ IDEA. This can be done by going to `Settings -> Build, Execution, Deployment -> Compiler -> Annotation Processors` and checking the `Enable annotation processing` checkbox.

## Set Lombok Path

The last step is to set the Lombok path in IntelliJ IDEA. This can be done by going to `Settings -> Build, Execution, Deployment -> Compiler -> Annotation Processors` and setting the path to the Lombok jar file.

## Rebuild Project

The final step is to rebuild the project in IntelliJ IDEA. This can be done by going to `Build -> Rebuild Project`. Once the project is rebuilt, it should compile without any errors.
