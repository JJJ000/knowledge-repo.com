---
title: Issue with Jackson JSON and hibernate jpa causing endless looping
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To prevent infinite recursion with Jackson JSON and Hibernate JPA, use the @JsonIgnore annotation on the entities` fields that reference each other.
---

**Contents**

[TOC]

### What is Infinite Recursion with Jackson JSON and Hibernate JPA?
Infinite recursion with Jackson JSON and Hibernate JPA is an issue that arises when serializing and deserializing Java objects with Jackson JSON and Hibernate JPA. The issue occurs when an object references itself, or another object, creating a loop that causes an infinite recursion.

### Causes of Infinite Recursion
The cause of infinite recursion is usually due to the way the object’s fields are mapped in the JPA annotations. For example, if an object has a field that references itself, this will cause an infinite recursion when the object is serialized. Another common cause is when an object has a field that references another object, and that other object has a field that references back to the original object.

### How to Avoid Infinite Recursion
In order to avoid infinite recursion, it is important to use the appropriate JPA annotations when mapping the object’s fields. For example, when an object has a field that references itself, the @JsonIgnore annotation should be used to prevent the object from being serialized. Additionally, when an object has a field that references another object, the @JsonManagedReference and @JsonBackReference annotations should be used to ensure that the objects are not serialized in a loop.

### Summary
Infinite recursion with Jackson JSON and Hibernate JPA is an issue that arises when serializing and deserializing Java objects. The issue is caused by objects referencing themselves or other objects in a loop, which causes an infinite recursion. To avoid this issue, it is important to use the appropriate JPA annotations when mapping the object’s fields.
