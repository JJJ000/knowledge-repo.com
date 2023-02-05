---
title: What is the syntax for indicating the Java compiler version in a pom.xml file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Java compiler version can be specified in the <build><plugins><plugin><configuration><source> and <target> tags of the pom.xml file.
---

**Contents**

[TOC]

##### Syntax

`<plugin>
  <groupId>org.apache.maven.plugins</groupId>
  <artifactId>maven-compiler-plugin</artifactId>
  <version>3.8.0</version>
  <configuration>
    <source>1.8</source>
    <target>1.8</target>
  </configuration>
</plugin>`

##### Explanation

The Maven Compiler Plugin is used to specify the version of Java that will be used to compile the project. The plugin is configured by adding the plugin to the `<plugins>` section of the `pom.xml` file. The `<source>` and `<target>` elements are used to specify the version of Java to be used for compilation. In the example above, the source and target versions are both set to 1.8, which indicates that the project will be compiled using Java 8.
