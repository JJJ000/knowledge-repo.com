---
title: How can I prevent a jpa field from being persisted?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The easiest way to ignore a JPA field during persistence is to annotate it with the @Transient annotation.
---

**Contents**

[TOC]

1. Annotation Based Solution 
    - Annotate the field with the `@Transient` annotation. This will signal to the JPA provider to ignore the field during persistence.

2. XML Based Solution 
    - Create an XML mapping file which declares the field as `transient`. This will signal to the JPA provider to ignore the field during persistence.
