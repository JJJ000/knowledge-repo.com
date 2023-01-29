---
title: How do hibernate and spring data jpa differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Hibernate is an ORM framework while Spring Data JPA is a wrapper around Hibernate that simplifies the development of data access layers.
---

**Contents**

[TOC]

### Hibernate
Hibernate is an open source Java persistence framework that provides a framework for mapping an object-oriented domain model to a relational database. It is an ORM (Object Relational Mapping) tool, which helps developers to persist their data into a relational database. It provides a powerful query language (HQL) that makes it easy to write queries to retrieve data. It also provides an API for managing transactions, caching, and synchronization with the database.

### Spring Data JPA
Spring Data JPA is a library of Spring that provides an abstraction layer over the Java Persistence API (JPA) and simplifies data access in applications that use JPA. It provides a repository abstraction layer that simplifies data access code and reduces the amount of boilerplate code needed to implement data access layers. It also provides support for the query language provided by JPA, as well as support for named queries and native queries. It also provides support for pagination and sorting of query results.
