---
title: Change the default spring-boot application.properties settings in a junit test
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Override default Spring-Boot application.properties settings in Junit Test in Java by using the @TestPropertySource annotation.
---

**Contents**

[TOC]

1. Overriding Properties in the Test Class
-------------------------------------------
You can override the default Spring-Boot application.properties settings in Junit Test in Java by annotating the test class with `@TestPropertySource` and pointing to the desired properties file.

2. Overriding Properties in the Test Method
-------------------------------------------
You can also override the default Spring-Boot application.properties settings in Junit Test in Java by annotating the test method with `@TestPropertySource` and pointing to the desired properties file.

3. Overriding Properties with Environment Variables
----------------------------------------------------
You can also override the default Spring-Boot application.properties settings in Junit Test in Java by setting environment variables in the test class or test method.

4. Overriding Properties with Java System Properties
---------------------------------------------------
You can also override the default Spring-Boot application.properties settings in Junit Test in Java by setting Java System Properties in the test class or test method.
