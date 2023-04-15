---
title: Hibernate generates a multiplebagfetchexception when attempting to fetch multiple collections at the same time
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Hibernate throws MultipleBagFetchException when trying to fetch multiple bags at the same time, as this is not supported.
---

**Contents**

[TOC]

### Overview
Hibernate is an open-source object-relational mapping (ORM) library for the Java language. It is used to map Java objects to relational database tables. Hibernate can throw a MultipleBagFetchException when attempting to fetch multiple bags from the database simultaneously.

### What is a Bag
A bag is an unordered collection of elements, similar to a List. A Bag does not guarantee that the elements will be in the same order when retrieved from the database.

### Causes of MultipleBagFetchException
The MultipleBagFetchException is thrown when Hibernate attempts to fetch multiple bags from the database simultaneously. This can occur if the query contains multiple joins, or if the query is attempting to fetch related entities that contain bags.

### Resolution
The MultipleBagFetchException can be resolved by avoiding simultaneous fetching of multiple bags. This can be done by restructuring the query to avoid multiple joins, or by fetching the data in separate queries. Additionally, it is possible to disable the MultipleBagFetchException by setting the hibernate.query.fail_on_multiple_bags system property to false.
