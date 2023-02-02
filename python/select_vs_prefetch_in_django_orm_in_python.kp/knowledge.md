---
title: What are the distinctions between using select_related and prefetch_related when utilizing the django orm?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: select\_related retrieves related objects in one query, while prefetch\_related retrieves related objects in multiple queries.
---

**Contents**

[TOC]

### select_related

select_related is a method used to retrieve related objects in one database query. It follows foreign-key relationships and is used to reduce the number of database queries required to retrieve related objects. It works by performing a SQL join, which can be used to retrieve all the related objects in a single query.

### prefetch_related

prefetch_related is similar to select_related in that it is used to retrieve related objects in one database query. However, prefetch_related follows many-to-many and many-to-one relationships and is used to reduce the number of database queries required to retrieve multiple related objects. It works by performing a SQL subquery, which can be used to retrieve all the related objects in a single query.
