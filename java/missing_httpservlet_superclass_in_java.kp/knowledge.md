---
title: The Java build path did not contain the superclass "javax.servlet.http.httpservlet"
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The javax.servlet.http.HttpServlet library must be added to the Java Build Path.
---

**Contents**

[TOC]

### Solution

### Step 1: Add the Servlet API to the Project

The first step is to add the servlet API to the project. This can be done by adding the servlet-api.jar file to the project's build path.

### Step 2: Add the Servlet API to the Classpath

The second step is to add the servlet-api.jar file to the classpath. This can be done by adding the jar file to the Java Runtime Environment (JRE) in the Java Build Path settings.

### Step 3: Restart the Project

The third step is to restart the project. This can be done by closing the project and re-opening it.

### Step 4: Test the Project

The fourth step is to test the project. This can be done by running the project and checking if the superclass "javax.servlet.http.HttpServlet" is found.
