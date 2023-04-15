---
title: What is the process for using Maven to build an executable jar file with its dependencies?
authors:
- nanja_dev
tags:
- java
- maven
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Maven Shade plugin to create an executable JAR with dependencies.
---

**Contents**

[TOC]

### Setting up your Maven Project

1. Create a new Maven project in your IDE.
2. Add the necessary dependencies to your `pom.xml` file.
3. Configure the `maven-jar-plugin` in the `pom.xml` file.

### Building the Executable JAR

1. Build the project with the command `mvn clean install`.
2. The executable JAR file will be located in the `target` directory.

### Running the Executable JAR

1. Run the executable JAR file with the command `java -jar <jar-file-name>.jar`.

### Packaging Dependencies in the Executable JAR

1. Configure the `maven-assembly-plugin` in the `pom.xml` file.
2. Build the project with the command `mvn clean package`.
3. The executable JAR file with dependencies will be located in the `target` directory.
