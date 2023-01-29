---
title: An exception has been thrown by jpa and hibernate indicating that an entity which is not attached has been sent to be persisted
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: An EntityExistsException is thrown when an attempt is made to persist a detached entity, indicating that the entity already exists in the database.
---

**Contents**

[TOC]

### What is a Detached Entity? 
A detached entity is an object that is no longer associated with a persistence context. This means that the entity is no longer managed by the persistence context and is no longer tracked by the underlying persistence provider. 

### What is the Persistent Object Exception?
The Persistent Object Exception is an exception thrown by the Java Persistence API (JPA) and Hibernate when an attempt is made to persist a detached entity. This exception is thrown because a detached entity is no longer associated with a persistence context and can no longer be tracked by the underlying persistence provider. 

### Why is it Thrown?
The Persistent Object Exception is thrown when an attempt is made to persist a detached entity because the entity is no longer associated with a persistence context and can no longer be tracked by the underlying persistence provider. 

### How to Avoid the Exception?
To avoid the Persistent Object Exception, the entity must be associated with a persistence context before attempting to persist it. This can be done by using the EntityManager.merge() method to merge the detached entity with the persistence context.
