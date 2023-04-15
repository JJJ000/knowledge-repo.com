---
title: What distinguishes @inject from @autowired in spring framework? when should each be used?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @Inject is used for dependency injection using annotations in Java, while @Autowired is used for dependency injection using the Autowired annotation in Spring Framework.
---

**Contents**

[TOC]

### @Inject
`@Inject` is a Java annotation from the JSR-330 standard. It is used for dependency injection and works with the javax.inject package. It is a standard annotation and is not specific to Spring.

### @Autowired
`@Autowired` is a Spring annotation used for dependency injection. It is specific to Spring and works with the org.springframework.beans package.

### When to Use
`@Inject` is typically used when you want to use a standard annotation for dependency injection. It is also useful when you want to use a third-party library that supports the JSR-330 standard.

`@Autowired` is typically used when you want to use a Spring-specific annotation for dependency injection. It is also useful when you want to use Spring-specific features such as autowiring by type, autowiring by name, and autowiring by constructor.
