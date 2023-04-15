---
title: What is the correct way to get the current username (securitycontext) information from a bean when using spring security?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The proper way to obtain current username information in a bean in Java using Spring Security is to use the SecurityContextHolder.getContext().getAuthentication().getName() method.
---

**Contents**

[TOC]

1. Setting Up Dependencies
----------------------------------
In order to use the SecurityContext, you must have the Spring Security dependency in your project. This can be done by adding the following dependency to your pom.xml:

```
<dependency>
    <groupId>org.springframework.security</groupId>
    <artifactId>spring-security-core</artifactId>
    <version>5.3.3.RELEASE</version>
</dependency>
```

2. Obtaining the SecurityContext
----------------------------------
Once you have the Spring Security dependency, you can obtain the SecurityContext in a bean by autowiring it into the bean:

```
@Autowired
private SecurityContext securityContext;
```

3. Retrieving the Username
----------------------------------
Once you have the SecurityContext, you can use the getAuthentication() method to retrieve the Authentication object. The Authentication object has a getName() method which returns the username of the currently logged in user:

```
String username = securityContext.getAuthentication().getName();
```

4. Accessing the Username
----------------------------------
Once you have the username, you can use it in your bean however you need. For example, you could use it to query a database for user-specific data:

```
User user = userRepository.findByUsername(username);
```
