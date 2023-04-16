---
title: No entitymanager linked to the current thread is associated with an active transaction, so the 'persist' call cannot be reliably processed
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `persist` call cannot be reliably processed without an EntityManager with an active transaction.
---

**Contents**

[TOC]

### Introduction 
EntityManager is a Java persistence API (JPA) interface that provides an object-relational mapping for the persistence of Java objects. It is used to manage the persistence of entities in a relational database. When a transaction is attempted, the EntityManager checks to see if there is an actual transaction available for the current thread. If there is not, then the EntityManager will not be able to reliably process the ‘persist’ call. 

### Causes 
The most common cause of this issue is when the EntityManager is not properly configured. If the EntityManager is not configured properly, it will not be able to detect the current transaction and will not be able to process the ‘persist’ call. 

Another possible cause is that the EntityManager is not properly configured to use the correct transaction manager. If the EntityManager is configured to use a different transaction manager than the one that is actually being used, then it will not be able to detect the current transaction and will not be able to process the ‘persist’ call. 

### Solutions
The first step in resolving this issue is to ensure that the EntityManager is properly configured. This includes making sure that the EntityManager is configured to use the correct transaction manager. 

Once the EntityManager is properly configured, the next step is to ensure that the current transaction is properly detected by the EntityManager. This can be done by making sure that the EntityManager is registered with the current transaction manager. 

Finally, if the issue persists, it is recommended to check the logs for any errors that may be related to the EntityManager. If any errors are found, they should be investigated further to determine the root cause of the issue. 

### Conclusion
No EntityManager with an actual transaction available for the current thread can be a difficult issue to resolve. However, by properly configuring the EntityManager and ensuring that the current transaction is detected, the issue can be resolved.
