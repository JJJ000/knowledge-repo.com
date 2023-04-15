---
title: In production, should hibernate be set to use the 'hbm2ddl.auto=update' setting?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It is not recommended to use hbm2ddl.auto=update in production, as it can cause unexpected changes to the database schema.
---

**Contents**

[TOC]

### Advantages
1. hbm2ddl.auto=update allows developers to make changes to the database structure without having to manually write the SQL queries.
2. This feature is especially useful in production environments, where manual changes to the database structure are not feasible.
3. It helps to keep the database structure up to date with the application code.

### Disadvantages
1. hbm2ddl.auto=update can be dangerous if used without caution, as it can lead to data loss.
2. It can also lead to unexpected changes to the database structure, which can cause unexpected errors and bugs.
3. If used incorrectly, hbm2ddl.auto=update can also lead to security vulnerabilities.
