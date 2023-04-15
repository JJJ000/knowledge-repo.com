---
title: Maven is unable to locate any junit tests to execute
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Maven requires explicit configuration in the pom.xml file to include JUnit tests in the build process.
---

**Contents**

[TOC]

### Solution

### Overview
Maven does not typically find JUnit tests to run in Java, as it does not have built-in support for running JUnit tests. However, it is possible to configure Maven to run JUnit tests by adding the necessary plugins and dependencies.

### Configuring Maven
In order to configure Maven to run JUnit tests, the following must be done:

1. Add the JUnit dependency to the project's POM file.
2. Add the Maven Surefire plugin to the project's POM file.
3. Configure the Surefire plugin to run the JUnit tests.

### Running JUnit Tests
Once the necessary plugins and dependencies have been added, the JUnit tests can be run using the following command:

```java
mvn test
```

### Conclusion
By following the steps above, it is possible to configure Maven to run JUnit tests in Java projects.
