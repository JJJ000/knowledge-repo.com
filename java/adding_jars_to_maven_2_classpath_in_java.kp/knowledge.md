---
title: Is it possible to include jars in the Maven 2 build classpath without having to install them?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Yes, you can add jars to the Maven 2 build classpath using the `dependency` tag in the project`s pom.xml file.
---

**Contents**

[TOC]

### Overview
Yes, it is possible to add jars to Maven 2 build classpath without installing them in Java. This can be done by including the jars in a Maven repository and then referencing them from the project's pom.xml file.

### Creating a Maven Repository
To add jars to the Maven 2 build classpath, you will need to create a Maven repository. This can be done by creating a folder on your local machine or server and adding the jars to it.

### Referencing the Jars in the pom.xml File
Once the repository has been created, you will need to reference the jars in the project's pom.xml file. This can be done by adding the following code to the pom.xml file:

```java
<dependencies>
    <dependency>
        <groupId>groupId</groupId>
        <artifactId>artifactId</artifactId>
        <version>version</version>
        <scope>system</scope>
        <systemPath>${project.basedir}/path/to/jar/jarName.jar</systemPath>
    </dependency>
</dependencies>
```

### Using the Jars in the Build
Once the jars have been referenced in the pom.xml file, they can be used in the Maven 2 build. The jars will be automatically included in the classpath and can be used by any code in the project.
