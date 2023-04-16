---
title: Specifying the active profile and configuration location from the command line in spring boot
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The active profile and config location can be set by passing the parameters -Dspring.profiles.active and -Dspring.config.location to the Java command.
---

**Contents**

[TOC]

# Section 1: Setting active profile

Spring Boot allows you to configure your application based on the environment it is running in. You can specify the active profile using the `spring.profiles.active` property in the application.properties file.

# Section 2: Config location

The `spring.config.location` property defines the location of the configuration files. This property can be set in the application.properties file or from the command line.

# Section 3: Command line

To set the active profile and config location from the command line, you can use the `-Dspring.profiles.active` and `-Dspring.config.location` options. For example, to set the active profile to "dev" and the config location to "/path/to/config":

```
java -jar myapp.jar -Dspring.profiles.active=dev -Dspring.config.location=/path/to/config
```

# Section 4: Java

You can also set the active profile and config location from Java code. To do this, you can use the `SpringApplication.setAdditionalProfiles` and `SpringApplication.setAdditionalProfiles` methods. For example:

```
SpringApplication app = new SpringApplication(MyApplication.class);
app.setAdditionalProfiles("dev");
app.setAdditionalProfiles("/path/to/config");
app.run(args);
```
