---
title: A collection with cascade="all-delete-orphan" was no longer associated with the entity instance that owned it in hibernate
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The orphaned collection elements will be deleted from the database when the owning entity instance is updated or deleted.
---

**Contents**

[TOC]

### What is Cascade=”all-delete-orphan”
Cascade=”all-delete-orphan” is an annotation in Hibernate that allows for operations to be cascaded from a parent entity to a child entity. This means that if the parent entity is deleted, the child entity will also be deleted. Additionally, if the child entity is no longer referenced by the parent entity, it will be deleted as an orphan.

### When is Cascade=”all-delete-orphan” Used?
Cascade=”all-delete-orphan” is typically used when there is a one-to-many relationship between two entities. This annotation ensures that when the parent entity is deleted, all of its child entities will also be deleted. Additionally, if the child entity is no longer referenced by the parent entity, it will be deleted as an orphan.

### What Happens When a Collection with Cascade=”all-delete-orphan” is No Longer Referenced by the Owning Entity Instance?
When a collection with Cascade=”all-delete-orphan” is no longer referenced by the owning entity instance, the child entities in the collection will be deleted. This is because the cascade setting is configured to delete any orphaned entities. Therefore, if the parent entity no longer references the child entities, they will be deleted.

### How to Prevent Orphaned Entities from Being Deleted?
To prevent orphaned entities from being deleted, the cascade setting can be changed from “all-delete-orphan” to “none”. This will prevent any cascading operations from taking place and the orphaned entities will remain in the database.
