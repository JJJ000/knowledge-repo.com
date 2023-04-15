---
title: What is the difference between @component and @bean annotations in spring?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @Component is used to denote a class as a Spring bean, while @Bean is used to register a bean to the Spring ApplicationContext.
---

**Contents**

[TOC]

### @Component

@Component is a Spring annotation used to denote a class as a component. It is used to mark a class as a Spring managed component. This means that the Spring container will manage the lifecycle of the component and its dependencies.

### @Bean

@Bean is a Spring annotation used to denote a method as a bean. It is used to mark a method as a bean definition for the Spring container. The method annotated with @Bean will be executed when the application context is created and the return value will be registered as a bean in the container.
