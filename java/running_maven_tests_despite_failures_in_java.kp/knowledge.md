---
title: Triggering Maven to execute all tests, even if some fail
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Maven can be configured to `fail-at-end` mode which will run all tests, even when some fail.
---

**Contents**

[TOC]

### Introduction

Maven is a popular build automation tool used in Java development. It is used to manage the build process, including compilation, testing, and packaging of code. When running tests with Maven, it is possible for some tests to fail. In this article, we will discuss how to make Maven run all tests, even when some fail.

### Configuring Maven to Run All Tests

Maven can be configured to run all tests, even when some fail, by adding the following configuration to the pom.xml file:

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-surefire-plugin</artifactId>
    <version>2.22.2</version>
    <configuration>
        <testFailureIgnore>true</testFailureIgnore>
    </configuration>
</plugin>
```

### Running the Tests

Once the configuration has been added, the tests can be run by executing the following command:

```
mvn clean test
```

### Conclusion

In this article, we discussed how to make Maven run all tests, even when some fail. We looked at how to configure Maven to ignore test failures, and how to run the tests with the updated configuration.
