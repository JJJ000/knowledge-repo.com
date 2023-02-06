---
title: How can I use jpa to map a native query result set to a collection of pojo classes?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The native query result set can be converted to a collection of POJO classes using the JPA EntityManager`s createNativeQuery() method.
---

**Contents**

[TOC]

### 1. Define the POJO Class

The first step to convert a native query result set to a POJO class collection is to define the POJO class. The POJO class should contain the same fields as the columns returned by the query, and should have getters and setters for each field.

### 2. Execute the Query

The next step is to execute the query and get the result set. This can be done using the EntityManager.createNativeQuery() method.

### 3. Map the Result Set to the POJO Class

The third step is to map the result set to the POJO class. This can be done using the ResultSetMapper.map() method. The ResultSetMapper takes a ResultSet and a POJO class, and returns a List of POJO objects.

### 4. Return the Collection

The final step is to return the collection of POJO objects. This can be done by returning the List of POJO objects created in the previous step.
