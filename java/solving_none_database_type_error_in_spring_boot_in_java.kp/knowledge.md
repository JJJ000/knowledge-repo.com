---
title: No embedded database driver class can be identified for database type none in spring boot
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No embedded database driver class can be determined for database type NONE.
---

**Contents**

[TOC]

## Solution

### 1. Use an Embedded Database

The easiest way to solve the problem of not being able to determine an embedded database driver class for a database type of NONE is to use an embedded database. An embedded database is a database that runs inside the same process as the application, rather than connecting to an external database. This eliminates the need to specify a database driver class, as the driver is embedded within the application itself.

### 2. Configure the Database

Once an embedded database has been chosen, it needs to be properly configured for use with Spring Boot. This involves setting the spring.datasource.url property in the application.properties file to the URL of the embedded database. Additionally, the spring.datasource.driverClassName property should be set to the driver class name of the embedded database.

### 3. Use an ORM Tool

Alternatively, an Object Relational Mapping (ORM) tool such as Hibernate or JPA can be used to access the embedded database. This eliminates the need to specify a database driver class, as the ORM tool will automatically generate the necessary code to access the database.

### 4. Use a Database Access Library

Finally, a database access library such as JDBC or jOOQ can be used to access the embedded database. This also eliminates the need to specify a database driver class, as the library will automatically generate the necessary code to access the database.
