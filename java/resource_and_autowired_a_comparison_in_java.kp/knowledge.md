---
title: Differences between @resource and @autowired
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @Resource is used for dependency injection by name, while @Autowired is used for dependency injection by type.
---

**Contents**

[TOC]

### Resource

`@Resource` is a Java annotation that allows you to inject resources into your application code, such as a data source or a service. It is part of the Java EE specification and can be used to inject resources into any Java class.

### Autowired

`@Autowired` is a Spring annotation that can be used to inject beans into your application code. It is part of the Spring framework and can be used to inject beans into any Java class.

### Difference

The main difference between `@Resource` and `@Autowired` is that `@Resource` is part of the Java EE specification and `@Autowired` is part of the Spring framework. `@Resource` can be used to inject resources into any Java class, while `@Autowired` can be used to inject beans into any Java class.
