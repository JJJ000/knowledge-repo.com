---
title: How do I create a 404 error in a spring-mvc controller?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Throw a new org.springframework.web.servlet.NoHandlerFoundException(`No handler found for this request`);
---

**Contents**

[TOC]

### Step 1: Create a Resource Not Found Page
Create a JSP page, or any other view technology, to display a message that the resource was not found.

### Step 2: Create a @ControllerAdvice
Create a `@ControllerAdvice` class that implements a `@ExceptionHandler` for the `NoHandlerFoundException`.

### Step 3: Redirect to the Resource Not Found Page
In the `@ExceptionHandler` method, redirect to the resource not found page created in Step 1.

### Step 4: Configure the Exception Handler
In the Spring configuration, add the `@ControllerAdvice` created in Step 2.
