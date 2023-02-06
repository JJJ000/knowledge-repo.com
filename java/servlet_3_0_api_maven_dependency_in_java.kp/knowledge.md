---
title: What is the Maven dependency for the servlet 3.0 api?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Maven dependency for Servlet 3.0 API in Java is `javax.servletjavax.servlet-api3.0.1`.
---

**Contents**

[TOC]

## Maven Repository
The Servlet 3.0 API is available in the Maven Central Repository.

## Dependency Declaration
In order to use the Servlet 3.0 API in a Maven project, the following dependency should be added to the project's `pom.xml` file:

```xml
<dependency>
    <groupId>javax.servlet</groupId>
    <artifactId>javax.servlet-api</artifactId>
    <version>3.0.1</version>
    <scope>provided</scope>
</dependency>
```

## Scope
The `scope` element of the dependency should be set to `provided` as the Servlet API is already included in the Java EE container.

## Version
The latest version of the Servlet 3.0 API is 3.0.1. It is recommended to use the latest version of the API in order to benefit from the latest bug fixes and features.
