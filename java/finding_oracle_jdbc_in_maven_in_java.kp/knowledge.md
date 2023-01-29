---
title: Search for the oracle jdbc driver in the Maven repository
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Oracle JDBC driver can be found in the Maven repository by searching for `com.oracle.ojdbcojdbc8`.
---

**Contents**

[TOC]

### Oracle Maven Repository

Oracle provides a Maven repository to make it easier to obtain Oracle JDBC drivers and other Oracle libraries. This repository is located at https://maven.oracle.com/.

### Adding the Repository to Your Maven Configuration

In order to use the Oracle Maven repository you need to add it to your Maven configuration. This can be done by adding the following to your `settings.xml` file:

```xml
<settings>
  <profiles>
    <profile>
      <id>oracle</id>
      <repositories>
        <repository>
          <id>maven-oracle-repo</id>
          <name>Oracle Maven Repository</name>
          <url>https://maven.oracle.com</url>
          <layout>default</layout>
          <releases>
            <enabled>true</enabled>
          </releases>
        </repository>
      </repositories>
    </profile>
  </profiles>
  <activeProfiles>
    <activeProfile>oracle</activeProfile>
  </activeProfiles>
</settings>
```

### Adding the Dependency

Once the repository is added to your Maven configuration, you can add the dependency for the Oracle JDBC driver. This can be done by adding the following to your `pom.xml` file:

```xml
<dependency>
  <groupId>com.oracle.jdbc</groupId>
  <artifactId>ojdbc6</artifactId>
  <version>11.2.0.4</version>
</dependency>
```

### Verifying the Installation

Once the dependency is added, you can verify the installation by running the following command:

```
mvn dependency:tree
```

This will output a list of all the dependencies and their versions. You should see the Oracle JDBC driver listed in the output.
