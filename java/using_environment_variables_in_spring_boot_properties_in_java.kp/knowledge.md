---
title: Incorporating environment variables into the spring boot application.properties file
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the Spring Expression Language (SpEL) to access environment variables in application.properties.
---

**Contents**

[TOC]

### Setting the Environment Variable

The first step is to set the environment variable in the environment where the application will run. This can be done in the command line, using the `export` command (for Linux systems):

```bash
export MY_VARIABLE="value"
```

For Windows systems, the `set` command can be used:

```batch
set MY_VARIABLE="value"
```

### Using the Environment Variable in application.properties

Once the environment variable is set, it can be used in the `application.properties` file. This can be done using the `${MY_VARIABLE}` syntax, where `MY_VARIABLE` is the name of the environment variable. For example:

```properties
spring.datasource.url=jdbc:mysql://localhost/${MY_VARIABLE}
```

### Accessing the Environment Variable in Java

The environment variable can also be accessed in Java code, using the `System.getenv()` method. This method takes the name of the environment variable as an argument and returns its value. For example:

```java
String myVariable = System.getenv("MY_VARIABLE");
```

### Using the Environment Variable in Spring Boot

In Spring Boot, the environment variable can be accessed using the `@Value` annotation. This annotation takes the name of the environment variable as an argument and injects its value into the corresponding field. For example:

```java
@Value("${MY_VARIABLE}")
private String myVariable;
```
