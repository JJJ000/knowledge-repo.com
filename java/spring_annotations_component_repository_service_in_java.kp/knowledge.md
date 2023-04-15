---
title: What are the distinctions between the @component, @repository, and @service annotations in Spring?
authors:
- nanja_dev
tags:
- java
- spring
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Spring, @Component is a generic annotation for any Spring-managed component, @Repository is a stereotype annotation for data access layers and @Service is a stereotype annotation for service layers.
---

**Contents**

[TOC]

### @Component
The @Component annotation is used to mark a Java class as a component. It is a generic stereotype for any Spring-managed component or bean. It is used to mark a class as a component so that it can be auto-detected through classpath scanning.

### @Repository
The @Repository annotation is used to indicate that the class provides the mechanism for storage, retrieval, search, update and delete operation on objects. It is used to mark a class as a repository so that it can be auto-detected through classpath scanning.

### @Service
The @Service annotation is used to indicate that the class provides the business logic for the application. It is used to mark a class as a service so that it can be auto-detected through classpath scanning.

### Differences
The main difference between the three annotations is that the @Component annotation is a generic stereotype for any Spring-managed component, while the @Repository and @Service annotations are more specific to their roles. The @Repository annotation is used to mark a class as a repository, while the @Service annotation is used to mark a class as a service.
