---
title: Retrieving specific columns using spring jpa
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Using the @ColumnResult annotation, specific columns can be selected from the query result in Spring JPA.
---

**Contents**

[TOC]

1. Introduction
Spring JPA is an ORM (Object Relational Mapping) tool used to simplify the data access layer of an application. It provides an abstraction over SQL queries and allows developers to write queries in Java instead of SQL.

2. Selecting Specific Columns
Spring JPA provides the ability to select specific columns from a database table. This can be done using the @ColumnResult annotation which is used to map the query result to an entity field. The @ColumnResult annotation is used to specify the column name and type of the column in the query result.

3. Example
For example, if we have a table called “Employee” with columns “id”, “name” and “salary” and we want to select the “name” and “salary” columns from the table, we can do so using the following query:

```
@Query("SELECT e.name, e.salary FROM Employee e")
List<Object[]> findNameAndSalary();
```

4. Conclusion
In this article, we discussed how to select specific columns from a database table using Spring JPA. We also looked at an example of how to do this.
