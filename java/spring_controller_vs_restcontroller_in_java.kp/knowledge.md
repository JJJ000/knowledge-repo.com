---
title: What are the distinctions between the spring @controller and @restcontroller annotations?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: @Controller is used for creating web applications, while @RestController is used for creating RESTful web services.
---

**Contents**

[TOC]

#1 @Controller

The @Controller annotation is used to mark a class as a Spring MVC controller. It is used to mark a class as a web request handler. It is used to map incoming web requests to specific handler methods.

#2 @RestController

The @RestController annotation is a specialized version of the @Controller annotation. It is used to create RESTful web services using Spring MVC. It is used to create RESTful web services that return JSON or XML response. It combines the @Controller and @ResponseBody annotations.

#3 Difference

The main difference between the two annotations is that the @Controller annotation is used to create web applications while the @RestController annotation is used to create RESTful web services. The @Controller annotation is used to map incoming web requests to specific handler methods while the @RestController annotation is used to create RESTful web services that return JSON or XML response.
