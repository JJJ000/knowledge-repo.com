---
title: What is the process for including local jar files in a Maven project?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Add the jar file to your local Maven repository, then add the dependency to your project`s pom.xml file.
---

**Contents**

[TOC]

### Step 1: Add the jar to the project

The first step is to add the jar file to the project. This can be done by copying the jar file to the project's `lib` folder. If the project does not have a `lib` folder, then you can create one.

### Step 2: Add the jar to the `pom.xml`

The next step is to add the jar to the `pom.xml` file. This can be done by adding the following code to the `<dependencies>` section of the `pom.xml` file:

```java
<dependency>
    <groupId>groupId</groupId>
    <artifactId>artifactId</artifactId>
    <version>version</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/lib/jar-file-name.jar</systemPath>
</dependency>
```

Be sure to replace `groupId`, `artifactId`, `version`, and `jar-file-name.jar` with the appropriate values.

### Step 3: Install the jar

The final step is to install the jar file. This can be done by running the following command in the terminal:

```java
mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=jar
```

Be sure to replace `<path-to-file>`, `<group-id>`, `<artifact-id>`, and `<version>` with the appropriate values.

Once this command is run, the jar file should be installed and available for use in the project.
