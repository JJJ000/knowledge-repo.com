---
title: Packaging dependencies into a jar file using maven
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Maven can be used to package dependencies into a jar file by including them in the <dependencies> section of the project`s pom.xml file.
---

**Contents**

[TOC]

### Adding Dependencies to pom.xml

The first step to including dependencies in a jar with Maven is to add the dependencies to the project’s pom.xml file. This is done by adding the appropriate <dependency> tags to the <dependencies> section of the pom.xml. The dependency tags should include the groupId, artifactId, version, and scope of the dependency. 

### Configuring the Jar Plugin

The next step is to configure the Maven Jar Plugin. This can be done by adding the appropriate <plugin> tags to the <plugins> section of the pom.xml. The plugin tags should include the groupId, artifactId, version, and configuration of the plugin. The configuration should include the <archive> tag and the <manifest> tag. The <archive> tag should specify the format of the jar file and the <manifest> tag should specify the main class that should be used when running the jar file. 

### Running the Jar Plugin

Once the dependencies and the Jar plugin are configured, the Jar plugin can be run by executing the following command: 

```java
mvn package
```

This will create a jar file in the `target` directory of the project.

### Running the Jar File

The jar file can then be run by executing the following command: 

```java
java -jar <jar-name>.jar
```

This will execute the main class specified in the <manifest> tag of the Jar plugin configuration. All of the dependencies included in the pom.xml will be included in the jar file.
