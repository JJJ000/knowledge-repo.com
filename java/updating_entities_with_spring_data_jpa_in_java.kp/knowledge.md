---
title: What is the process for updating an entity using spring-data-jpa?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the save() method of the JpaRepository to update an entity using spring-data-jpa in Java.
---

**Contents**

[TOC]

`**` Retrieve the Entity**

To update an entity using Spring Data JPA, the entity must first be retrieved from the database. This can be done using the `findById` method of the `JpaRepository` interface. This method takes an `id` as an argument and returns an `Optional` containing the entity with the given `id`.

`**` Modify the Entity**

Once the entity is retrieved, it can be modified by setting the desired values in the entity object.

`**` Save the Entity**

The modified entity can then be saved back to the database using the `save` method of the `JpaRepository` interface. This method takes the entity object as an argument and returns the saved entity.

`**` Refresh the Entity**

Finally, the entity must be refreshed in order to ensure that the latest version of the entity is available in the persistence context. This can be done using the `refresh` method of the `EntityManager` interface. This method takes the entity object as an argument and refreshes its state from the database.
