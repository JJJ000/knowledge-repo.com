---
title: What occurs behind the scenes when using the @transactional annotation in the spring framework?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: When a method is annotated with @Transactional, a proxy is created to manage the transaction in the background.
---

**Contents**

[TOC]

1. Transaction Propagation
 
When @Transactional is used, the Spring framework will set up a proxy for the given class and all public methods will be marked as transactional. This means that Spring will manage the transaction lifecycle and will propagate transaction settings from one method to another.

2. Transaction Management

The Spring framework will manage the transaction lifecycle, meaning that it will handle the start and end of the transaction. It will also manage the commit or rollback of the transaction depending on the outcome of the method.

3. Transaction Isolation

The Spring framework will also manage the transaction isolation level. This means that the framework will ensure that concurrent transactions do not conflict with each other.

4. Transaction Synchronization

The Spring framework will also manage the transaction synchronization. This means that the framework will ensure that the transaction is synchronized with the current thread and will ensure that the transaction is committed or rolled back at the end of the thread.
