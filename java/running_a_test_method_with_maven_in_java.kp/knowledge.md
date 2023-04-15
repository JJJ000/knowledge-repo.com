---
title: Execute a single test case using maven
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run a single test method with Maven in Java by using the command `mvn -Dtest=<TestClassName>#<testMethodName> test`.
---

**Contents**

[TOC]

### Prerequisites
1. Ensure that you have the correct version of Java installed.
2. Ensure that you have maven installed.

### Set Up
1. Navigate to the project directory.
2. Open the pom.xml file.
3. Add the following line to the pom.xml file:
    ```java
    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-plugin</artifactId>
        <version>2.22.1</version>
        <configuration>
            <test>
                <className>FullyQualifiedClassName#testMethodName</className>
            </test>
        </configuration>
    </plugin>
    ```

### Run Test
1. From the command line, run the following command:
    ```java
    mvn test
    ```
2. The test will run and the results will be displayed in the command line.
