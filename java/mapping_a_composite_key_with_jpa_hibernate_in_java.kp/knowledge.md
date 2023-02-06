---
title: What is the process for mapping a composite key using jpa and hibernate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A composite key can be mapped using a @Embeddable annotation and @EmbeddedId annotation in JPA and Hibernate.
---

**Contents**

[TOC]

### Section 1: Defining the Composite Key

The composite key is an entity that is used to uniquely identify a database record. It is composed of two or more columns that together form a primary key. In JPA and Hibernate, the composite key is defined using the @Embeddable and @EmbeddedId annotations.

### Section 2: Creating the Embeddable Class

The first step in mapping a composite key is to create an Embeddable class. This class should define the fields for the composite key and should be annotated with the @Embeddable annotation.

### Section 3: Mapping the Embeddable Class

Once the Embeddable class is created, it needs to be mapped to the entity class. This is done by adding the @EmbeddedId annotation to the entity class and specifying the name of the Embeddable class as the value of the annotation.

### Section 4: Defining the Primary Key

The final step is to define the primary key in the entity class. This is done using the @Id annotation and specifying the name of the field that contains the composite key.
