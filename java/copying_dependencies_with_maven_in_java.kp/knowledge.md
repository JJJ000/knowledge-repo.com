---
title: Have Maven copy dependencies into target/lib
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run the maven-dependency-plugin with the copy-dependencies goal to copy all dependencies into the target/lib directory.
---

**Contents**

[TOC]

# Section 1: Add Dependency Plugin

To make Maven copy dependencies into target/lib, the [dependency plugin](https://maven.apache.org/plugins/maven-dependency-plugin/) must be added to the Maven project. This plugin can be added by adding the following to the `<plugins>` section of the `pom.xml` file.

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-dependency-plugin</artifactId>
    <version>3.1.1</version>
</plugin>
```

# Section 2: Add Copy Dependencies Goal

The next step is to add the `copy-dependencies` goal to the `pom.xml` file. This goal will copy the dependencies specified in the `pom.xml` file into the `target/lib` directory. The `copy-dependencies` goal can be added by adding the following to the `<plugins>` section of the `pom.xml` file.

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-dependency-plugin</artifactId>
    <version>3.1.1</version>
    <executions>
        <execution>
            <id>copy-dependencies</id>
            <phase>package</phase>
            <goals>
                <goal>copy-dependencies</goal>
            </goals>
            <configuration>
                <outputDirectory>${project.build.directory}/lib</outputDirectory>
            </configuration>
        </execution>
    </executions>
</plugin>
```

# Section 3: Run Maven Package Goal

Once the `copy-dependencies` goal has been added to the `pom.xml`, the `package` goal must be run in order for the dependencies to be copied into the `target/lib` directory. This can be done by running the following command:

```
mvn package
```

# Section 4: Verify Dependencies Copied

Once the `package` goal has been run, the `target/lib` directory should contain the dependencies specified in the `pom.xml` file. This can be verified by using a file explorer to navigate to the `target/lib` directory.
