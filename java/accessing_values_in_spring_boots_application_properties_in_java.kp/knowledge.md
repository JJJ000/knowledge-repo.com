---
title: How can I retrieve a value from the application.properties file in spring boot?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can access a value defined in the application.properties file in Spring Boot in Java by using the @Value annotation.
---

**Contents**

[TOC]

1. **Create a class to hold the value**

Create a class to hold the value from the application.properties file. This class should be annotated with `@ConfigurationProperties` annotation.

2. **Create a bean**

Create a bean for the class created in step 1. This bean should be annotated with `@Bean` annotation.

3. **Autowire the bean**

Autowire the bean in the class where the value is required.

4. **Access the value**

Finally, access the value using the bean's getter method.
