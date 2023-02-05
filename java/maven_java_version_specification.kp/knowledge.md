---
title: Understanding the differences between specifying Java version in Maven using properties and the compiler plugin
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The maven-compiler-plugin is used to set the version of Java used to compile the code, while the Maven properties are used to set the version of Java used to execute the code.
---

**Contents**

[TOC]

### Using Properties
The Java version used in Maven can be specified by setting the `java.version` property in the `<properties>` section of the `pom.xml` file. This property can be used to specify the version of Java that should be used to run the project. 

For example:
```
<properties>
    <java.version>1.8</java.version>
</properties>
```

### Using Compiler Plugin
The Java version used in Maven can also be specified by using the `maven-compiler-plugin` plugin. This plugin allows for more control over the version of Java used to compile the project. 

For example:
```
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <version>3.8.0</version>
    <configuration>
        <source>1.8</source>
        <target>1.8</target>
    </configuration>
</plugin>
```
