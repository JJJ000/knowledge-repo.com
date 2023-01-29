---
title: Comparing jpa and hibernate criteria queries with jpql or hql
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: JPQL and HQL are both object-oriented query languages, while Criteria is a type-safe, programmatic way of expressing queries.
---

**Contents**

[TOC]

### Criteria

Criteria API is a type-safe way of expressing queries in the Java programming language. It is used to create and execute object-oriented queries. It is part of the Java Persistence API (JPA) and is used to define queries that are independent of any particular data store. It provides a simple API for creating and executing queries, as well as a set of classes and interfaces for defining query parameters.

### JPQL or HQL

JPQL or HQL (Hibernate Query Language) is a query language used to access data stored in a relational database. It is similar to SQL, but is object-oriented and uses Java classes and objects instead of tables and columns. JPQL is a subset of HQL and is used to access data from a relational database. It is used to create and execute queries that are independent of any particular data store. It provides a simple API for creating and executing queries, as well as a set of classes and interfaces for defining query parameters.

### Advantages of Criteria over JPQL or HQL

1. Type-Safety: Criteria API is type-safe, which means that it verifies the correctness of the query at compile time. This eliminates the possibility of runtime errors due to incorrect query syntax.

2. Readability: Criteria API is more readable than JPQL or HQL, as it is written in Java code. This makes it easier to understand and debug.

3. Flexibility: Criteria API is more flexible than JPQL or HQL, as it allows for dynamic query building. This makes it easier to modify queries based on user input.

4. Performance: Criteria API is more efficient than JPQL or HQL, as it does not require the query to be parsed and compiled at runtime. This results in improved performance.
