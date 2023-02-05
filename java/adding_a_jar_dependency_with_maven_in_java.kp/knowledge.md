---
title: Maven add a jar dependency using a relative path
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Maven cannot add a dependency to a jar by relative path in Java.
---

**Contents**

[TOC]

### Adding a Dependency in Maven

Maven is a popular build automation tool used for Java projects. It allows developers to easily manage project dependencies and build Java applications.

### Adding a Dependency by Relative Path

To add a dependency to a jar by relative path in Java using Maven, you first need to add the jar to your project’s lib directory. Then, you need to add the following code to your pom.xml file:

```
<dependency>
    <groupId>com.example</groupId>
    <artifactId>example-jar</artifactId>
    <version>1.0.0</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/lib/example-jar.jar</systemPath>
</dependency>
```

Replace `example-jar` with the name of your jar file and `1.0.0` with the version of your jar file.

### Verifying the Dependency

Once you have added the dependency to your project, you can verify that it is working correctly by running the following command:

```
mvn dependency:tree
```

This command will list all of the dependencies in your project, including the one you just added. If the jar file is listed, then the dependency has been successfully added.
