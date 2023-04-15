---
title: Using the @transactional annotation in spring to set the isolation and propagation levels
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @Transactional provides the ability to control the isolation level and propagation behavior of a transaction in Java.
---

**Contents**

[TOC]

### Isolation

Spring @Transactional provides isolation levels to ensure that transactions are processed reliably and consistently. Isolation levels define how transactions interact with each other and the data they access.

The most commonly used isolation levels are:

- READ_UNCOMMITTED
- READ_COMMITTED
- REPEATABLE_READ
- SERIALIZABLE

### Propagation

Spring @Transactional provides propagation levels to define how transactions interact with each other. Propagation levels define the behavior of a transaction when it is called from an existing transaction.

The most commonly used propagation levels are:

- REQUIRED
- REQUIRES_NEW
- MANDATORY
- NESTED
- SUPPORTS
- NOT_SUPPORTED
