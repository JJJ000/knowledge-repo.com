---
title: What are the distinctions between adding a property to application.yml or bootstrap.yml in a spring boot project?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Application.yml contains application-specific configuration, while bootstrap.yml contains configuration related to the Spring Boot application itself.
---

**Contents**

[TOC]

### Application.yml
Application.yml is a configuration file that is used to define the application level properties. It is used for configuring the application’s environment and the application’s behavior. It allows us to define different profiles for different environments. It is also used to define the application’s logging, security, and database configurations.

### Bootstrap.yml
Bootstrap.yml is a configuration file that is used to define the bootstrap level properties. It is used to define the behavior of the Spring Boot application before the application context is created. It allows us to define the configuration that needs to be loaded before the application context is created. It is also used to define the logging, security, and database configurations.
