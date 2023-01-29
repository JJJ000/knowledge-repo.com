---
title: What is the command to instruct Maven to utilize the most recent version of a dependency?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the version range syntax in the dependency`s version element, such as [1.0.0,2.0.0).
---

**Contents**

[TOC]

### Step 1: Declare the Dependency

Declare the dependency in the `pom.xml` file of the project.

```xml
<dependency>
  <groupId>org.example.dependency</groupId>
  <artifactId>example-dependency</artifactId>
  <version>LATEST</version>
</dependency>
```

### Step 2: Configure the Dependency

Configure the dependency in the `settings.xml` file of the Maven installation.

```xml
<settings>
  <profiles>
    <profile>
      <id>example-dependency</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <repositories>
        <repository>
          <id>example-dependency-repo</id>
          <url>http://example.com/repo</url>
          <releases>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
          </releases>
        </repository>
      </repositories>
    </profile>
  </profiles>
</settings>
```

### Step 3: Update the Repository

Update the repository using the `mvn clean install` command.

### Step 4: Resolve the Dependency

Resolve the dependency using the `mvn dependency:resolve` command.
