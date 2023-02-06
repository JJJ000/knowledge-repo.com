---
title: What is the most efficient way to access the current active/default environment profile in spring?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The active/default Environment profile can be obtained using the getActiveProfiles() method of the Environment interface.
---

**Contents**

[TOC]

1. Overview 
2. Setup 
3. Retrieve Profile Programmatically 
4. Conclusion 

### Overview 
Spring provides a powerful feature to manage different environment profiles for an application. This allows developers to create different configuration files for different profiles such as 'dev', 'prod', 'qa', etc. and switch between them easily. This makes it easier to manage the different configurations for different environments. 

### Setup 
In order to use environment profiles in Spring, you need to create a `application.properties` file in the resources folder. This file should contain all the configuration parameters for each environment profile. You can then add the profile specific configuration parameters in separate files such as `application-dev.properties`, `application-prod.properties`, etc. 

### Retrieve Profile Programmatically 
In order to retrieve the current active/default environment profile programmatically in Spring in Java, you can use the `@Profile` annotation. This annotation can be used to specify the active profile for a particular bean. For example, if you want to retrieve the active profile for a particular bean, you can add the `@Profile` annotation to the bean with the profile name as the value. 

For example: 
```java
@Bean
@Profile("dev")
public MyBean getMyBean() {
    return new MyBean();
}
```

You can then use the `Environment` class to retrieve the active profile. The `Environment` class provides the `getActiveProfiles()` method which can be used to get the list of active profiles. For example: 

```java
@Autowired
private Environment env;

String[] activeProfiles = env.getActiveProfiles();
```

### Conclusion
In this article, we discussed how to get the current active/default environment profile programmatically in Spring in Java. We saw how to setup environment profiles in Spring and how to use the `@Profile` annotation to retrieve the active profile. Finally, we saw how to use the `Environment` class to retrieve the active profile.
