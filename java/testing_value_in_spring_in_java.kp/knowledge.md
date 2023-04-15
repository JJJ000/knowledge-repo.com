---
title: Testing the values assigned to spring @value during a unit test
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Unit tests can use MockEnvironment to populate @Value fields with test values.
---

**Contents**

[TOC]

### Accessing @Value in Unit Test

In order to access the @Value annotation in a unit test, the Spring Context must be loaded. This can be done by annotating the unit test class with the `@ContextConfiguration` annotation. The `@ContextConfiguration` annotation requires the configuration class to be passed as an argument. This configuration class should contain the beans and properties needed for the unit test.

### Populating the @Value

The @Value annotation can be populated by setting the value in the configuration class. This can be done by using the `@PropertySource` annotation and providing the path to the properties file. The properties file should contain the key-value pairs for the @Value annotation.

### Using @TestPropertySource

The @TestPropertySource annotation can be used to provide the properties file for the @Value annotation. This annotation will override the values from the configuration class. This is useful when running unit tests on different environments.

### Using Environment Variables

Environment variables can also be used to populate the @Value annotation. This can be done by setting the environment variable in the unit test class and then accessing it in the configuration class. The environment variable should be set with the `@TestPropertySource` annotation.
