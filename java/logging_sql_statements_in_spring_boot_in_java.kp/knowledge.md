---
title: What is the process for recording sql statements in spring boot?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can log SQL statements in Spring Boot in Java by setting the logging.level.org.hibernate.SQL property to DEBUG.
---

**Contents**

[TOC]

### Using Logging

Spring Boot provides a logging feature that allows you to log SQL statements. To enable logging of SQL statements, you need to set the logging level to DEBUG. This can be done in the application.properties file, as shown below:

logging.level.org.hibernate.SQL=DEBUG

### Using a Custom Interceptor

Another way to log SQL statements in Spring Boot is to create a custom interceptor. This interceptor can be used to log SQL statements before and after they are executed. To create the interceptor, you need to create a class that implements the org.hibernate.Interceptor interface. This class will then be registered with the SessionFactory.

### Using Spring AOP

Yet another way to log SQL statements in Spring Boot is to use Spring AOP. This can be done by creating an aspect that implements the org.aspectj.lang.annotation.AfterThrowing annotation. This annotation can be used to log SQL statements before and after they are executed.

### Using a Database Profiler

Finally, you can also use a database profiler to log SQL statements in Spring Boot. A database profiler is a tool that can be used to monitor and analyze the performance of database queries. It can be used to log SQL statements and their execution times.
