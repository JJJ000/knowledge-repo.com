---
title: Using hibernate and mysql, how can I create and update timestamps?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Hibernate can be used to automatically set the values of creation and last update timestamps in the database using the @CreationTimestamp and @UpdateTimestamp annotations.
---

**Contents**

[TOC]

### Creating the Database Table

To create a database table with a creation and last update timestamp, you need to add two columns to the table. The columns should be of type `TIMESTAMP` and should have the `DEFAULT CURRENT_TIMESTAMP` and `ON UPDATE CURRENT_TIMESTAMP` clauses.

```sql
CREATE TABLE table_name (
    id INT AUTO_INCREMENT,
    creation_timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    last_update_timestamp TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    ...
    PRIMARY KEY (id)
);
```

### Mapping the Database Table to the Java Entity

To map the database table to the Java entity, you need to add two fields to the entity, annotated with `@CreationTimestamp` and `@UpdateTimestamp`.

```java
@Entity
public class EntityName {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @CreationTimestamp
    private LocalDateTime creationTimestamp;

    @UpdateTimestamp
    private LocalDateTime lastUpdateTimestamp;
    
    ...
}
```

### Saving and Updating Entities

To save and update entities, you need to use the `EntityManager` and `EntityTransaction` APIs. 

When saving an entity, the `EntityManager` will automatically set the `creationTimestamp` field to the current timestamp. When updating an entity, the `EntityManager` will automatically set the `lastUpdateTimestamp` field to the current timestamp.

```java
EntityManager em = emf.createEntityManager();
EntityTransaction tx = em.getTransaction();
tx.begin();

// save entity
em.persist(entity);

// update entity
em.merge(entity);

tx.commit();
em.close();
```

### Retrieving Entities

To retrieve entities with their timestamps, you can use the `EntityManager` API.

```java
EntityManager em = emf.createEntityManager();
EntityTransaction tx = em.getTransaction();
tx.begin();

Entity entity = em.find(Entity.class, id);

tx.commit();
em.close();
```

The `creationTimestamp` and `lastUpdateTimestamp` fields of the entity will be populated with the corresponding values from the database.
