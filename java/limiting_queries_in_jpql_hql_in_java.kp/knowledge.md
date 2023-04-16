---
title: What is the syntax for performing a limit query in jpql or hql?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In JPQL or HQL, a limit query can be done by using the `SET MAX\_RESULTS` clause.
---

**Contents**

[TOC]

**Section 1: Overview**
JPQL (Java Persistence Query Language) and HQL (Hibernate Query Language) are two object-oriented query languages used to query data from a database. They are used to retrieve data from tables and objects in a database. Both JPQL and HQL are similar to SQL in syntax and can be used to create, read, update, and delete data in a database.

**Section 2: JPQL Limit Query**
A JPQL limit query is used to limit the number of results returned from a query. The syntax for a JPQL limit query is as follows:

SELECT * FROM table_name [WHERE condition] ORDER BY column_name [ASC/DESC] LIMIT number_of_records;

**Section 3: HQL Limit Query**
An HQL limit query is used to limit the number of results returned from a query. The syntax for an HQL limit query is as follows:

SELECT * FROM table_name [WHERE condition] ORDER BY column_name [ASC/DESC] FETCH FIRST number_of_records ROWS ONLY;

**Section 4: Examples**
JPQL limit query example:

SELECT * FROM Student WHERE age > 18 ORDER BY name ASC LIMIT 10;

HQL limit query example:

SELECT * FROM Student WHERE age > 18 ORDER BY name ASC FETCH FIRST 10 ROWS ONLY;
