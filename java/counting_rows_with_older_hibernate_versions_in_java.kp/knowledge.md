---
title: What is the method for counting rows in older versions of hibernate (prior to 2009)?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: We can count rows using older versions of Hibernate (~2009) in Java by using the Query.setMaxResults() method to set a limit on the number of results returned.
---

**Contents**

[TOC]

**Using Criteria API**

1. Create a Criteria object with the class of the entity being queried:
```java
Criteria criteria = session.createCriteria(EntityClass.class);
```

2. Set Projection to count the rows:
```java
criteria.setProjection(Projections.rowCount());
```

3. Execute the query and get the row count:
```java
Long rowCount = (Long) criteria.uniqueResult();
```

**Using HQL**

1. Create a Query object with the HQL query to count the rows:
```java
Query query = session.createQuery("select count(*) from EntityClass");
```

2. Execute the query and get the row count:
```java
Long rowCount = (Long) query.uniqueResult();
```
