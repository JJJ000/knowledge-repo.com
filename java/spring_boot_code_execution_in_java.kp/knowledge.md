---
title: Executing code once spring boot has initialized
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Annotate a method with @PostConstruct to have it execute after Spring Boot starts.
---

**Contents**

[TOC]

### Adding a CommandLineRunner

The easiest way to run code after Spring Boot starts is to create a CommandLineRunner. This is an interface with a single run() method. The run() method will be called just after the application context is loaded. 

To add a CommandLineRunner, create a new class and add the @Component annotation. This will cause Spring Boot to detect the class and automatically add it to the application context. Then, implement the CommandLineRunner interface and add the run() method.

### Adding a StartupRunner

Another way to run code after Spring Boot starts is to create a StartupRunner. This is a class that implements the ApplicationRunner interface. The run() method of this interface will be called just after the application context is loaded. 

To add a StartupRunner, create a new class and add the @Component annotation. This will cause Spring Boot to detect the class and automatically add it to the application context. Then, implement the ApplicationRunner interface and add the run() method.

### Adding a @PostConstruct Annotation

The third way to run code after Spring Boot starts is to add a @PostConstruct annotation to a method. This annotation will cause the method to be called just after the application context is loaded. 

To add a @PostConstruct annotation, create a new class and add the @Component annotation. This will cause Spring Boot to detect the class and automatically add it to the application context. Then, add the @PostConstruct annotation to a method in the class.

### Adding a @EventListener Annotation

The fourth way to run code after Spring Boot starts is to add a @EventListener annotation to a method. This annotation will cause the method to be called when a specific event is fired. 

To add a @EventListener annotation, create a new class and add the @Component annotation. This will cause Spring Boot to detect the class and automatically add it to the application context. Then, add the @EventListener annotation to a method in the class. The @EventListener annotation takes a parameter which is the type of event to listen for. When the specified event is fired, the method will be called.
