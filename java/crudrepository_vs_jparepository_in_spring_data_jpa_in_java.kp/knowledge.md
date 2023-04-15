---
title: What are the distinctions between crudrepository and jparepository in spring data jpa?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: CrudRepository provides basic CRUD functionality, while JpaRepository provides JPA-specific functionality, such as the ability to flush and clear the persistence context.
---

**Contents**

[TOC]

#1 Overview 
CrudRepository and JpaRepository are both interfaces in Spring Data JPA that provide methods for data access and manipulation. The main difference between them is that CrudRepository provides basic CRUD (Create, Read, Update, Delete) operations, while JpaRepository provides more advanced functionality, such as query methods and pagination. 

#2 CRUD Operations 
CrudRepository provides basic CRUD operations such as save, findOne, findAll, delete and deleteAll. It also provides a few other methods such as exists and count. 

JpaRepository provides the same CRUD operations as CrudRepository, but it also provides more advanced operations such as query methods and pagination. It also provides additional methods for managing the persistence context such as flush, clear and detach. 

#3 Query Methods 
CrudRepository does not provide any query methods, so you will need to write your own custom queries to perform data access operations. 

JpaRepository provides a wide range of query methods that allow you to perform data access operations without having to write custom queries. It also provides support for named queries and native queries. 

#4 Pagination 
CrudRepository does not provide any pagination methods, so you will need to write your own custom queries to perform pagination. 

JpaRepository provides pagination methods such as findAll(Pageable pageable) and findAll(Example example, Pageable pageable). These methods allow you to easily perform pagination without having to write custom queries.
