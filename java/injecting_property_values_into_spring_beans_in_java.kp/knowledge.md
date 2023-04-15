---
title: What is the process for assigning a property value to a spring bean that has been set up using annotations?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can inject a property value into a Spring Bean configured using annotations by using the @Value annotation.
---

**Contents**

[TOC]

### Create the Bean

In order to inject a property value into a Spring Bean, the Bean must first be created. This can be done using annotations in Java.

### Annotate the Bean

The Bean must be annotated with the `@Component` annotation in order to make it eligible for dependency injection. It can also be annotated with the `@Value` annotation to define the property value that should be injected.

### Configure the Application

The application must be configured to enable the use of annotations. This can be done by adding the `@EnableAnnotation` annotation to the application configuration class.

### Inject the Property

Once the Bean is created and annotated, and the application is configured, the property value can be injected into the Bean by using the `@Autowired` annotation.
