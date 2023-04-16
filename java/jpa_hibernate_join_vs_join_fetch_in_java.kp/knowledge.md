---
title: What are the distinctions between using join and join fetch in jpa and hibernate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JOIN is used to return the results of a query as a flat result set, while JOIN FETCH is used to return the results of a query as a graph of objects.
---

**Contents**

[TOC]

# JOIN
A JOIN is used to retrieve data from two or more tables. It combines records from two or more tables in a database based on a common field between them. A JOIN query will return all rows from multiple tables where the join condition is met.

# JOIN FETCH
JOIN FETCH is an optimization technique used to retrieve data from multiple tables in a single query. It is used to reduce the number of database queries required to retrieve data from multiple tables. With JOIN FETCH, the data from the joined tables is retrieved in a single query and stored in a single object. This object can then be used to access the data from the joined tables.
