---
title: What are the drawbacks of using spring's applicationcontext.getbean?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: ApplicationContext.getBean is considered bad because it tightly couples the code to the Spring Framework, making it difficult to test and maintain.
---

**Contents**

[TOC]

**1. Unclear Ownership:**
ApplicationContext.getBean() returns a generic object and does not indicate who is responsible for creating and managing the object. This makes it difficult to determine who is responsible for the object's lifecycle and maintenance.

**2. Unmanaged Dependencies:**
ApplicationContext.getBean() does not manage dependencies between beans. This means that it is possible for a bean to be created without any of its dependencies being initialized. This can lead to unexpected behaviours and errors.

**3. Poor Performance:**
ApplicationContext.getBean() can be slow and inefficient. It requires the context to search through all of its beans to find the desired one, which can be time consuming.

**4. Brittle Code:**
ApplicationContext.getBean() is prone to breaking if the underlying bean structure changes. If a bean is removed or renamed, the code that uses ApplicationContext.getBean() will need to be updated accordingly. This can lead to brittle code that is difficult to maintain.
