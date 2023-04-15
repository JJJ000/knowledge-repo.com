---
title: The difference between <contextannotation-config> and <contextcomponent-scan> is that the former enables annotation-based configuration while the latter enables component scanning for autodetecting classes and registering bean definitions
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The <contextannotation-config> enables support for @Configuration, @Component, @Autowired and other annotations, while the <contextcomponent-scan> scans for classes annotated with @Component, @Repository, @Service, and @Controller and registers them as beans in the application context.
---

**Contents**

[TOC]

### <context:annotation-config>
The <context:annotation-config> element is used to enable annotation-driven configuration in the application context. It enables the use of annotations such as @Autowired, @Required, @PostConstruct, @PreDestroy and @Value in the application context.

### <context:component-scan>
The <context:component-scan> element is used to scan for annotated components in the application context. It scans for classes annotated with @Component, @Service, @Repository, @Controller, etc. and registers them as beans in the application context.

### Difference
The main difference between the two is that <context:annotation-config> enables annotation-driven configuration in the application context, while <context:component-scan> scans for annotated components in the application context and registers them as beans.
