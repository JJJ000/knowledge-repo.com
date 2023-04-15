---
title: What does the pluginmanagement tag do in maven's pom.xml?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: PluginManagement in Maven`s pom.xml is used to manage plugin versions and configuration across multiple projects.
---

**Contents**

[TOC]

### Definition
PluginManagement is a section in Maven's pom.xml that allows declaring the plugins that should be used for building the project. This section is used to configure plugins that should be used for all projects in a multi-module build.

### Benefits
The main benefit of using pluginManagement in Maven is that it allows developers to define the plugins that should be used across multiple projects in a single place. This eliminates the need to configure plugins in each project individually. Additionally, pluginManagement allows developers to set default configuration parameters for plugins, which can be overridden in individual projects.

### Usage
PluginManagement should be used to declare and configure plugins that should be used across multiple projects in a multi-module build. It is important to note that plugins declared in the pluginManagement section will not be automatically applied to projects. Plugins must be explicitly declared in the build section of each project's pom.xml in order to be used.

### Example
The following example shows how to declare the maven-compiler-plugin in the pluginManagement section of a pom.xml file:

```
<pluginManagement>
  <plugins>
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.5.1</version>
      <configuration>
        <source>1.8</source>
        <target>1.8</target>
      </configuration>
    </plugin>
  </plugins>
</pluginManagement>
```
