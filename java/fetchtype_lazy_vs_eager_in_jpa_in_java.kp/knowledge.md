---
title: What is the distinction between fetchtype lazy and eager when using the Java persistence api?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: FetchType LAZY indicates that data should be fetched lazily while FetchType EAGER indicates that data should be fetched eagerly.
---

**Contents**

[TOC]

#FetchType LAZY
FetchType LAZY is a type of fetching strategy in Java Persistence API (JPA) which specifies that data should be fetched lazily i.e. when it is actually needed. This means that when an entity is fetched, its related entities are not fetched immediately. Instead, they are fetched when they are actually needed. This improves the performance of the application as it reduces the amount of data that needs to be fetched from the database.

#FetchType EAGER
FetchType EAGER is a type of fetching strategy in Java Persistence API (JPA) which specifies that data should be fetched eagerly i.e. when the entity is fetched, its related entities are also fetched immediately. This means that all the data related to an entity is fetched from the database at once, which can lead to a large amount of data being fetched from the database. This can lead to poor performance of the application as it can take a long time to fetch the data from the database.

#Difference
The main difference between FetchType LAZY and FetchType EAGER is that FetchType LAZY fetches data lazily i.e. when it is actually needed, while FetchType EAGER fetches data eagerly i.e. all related data is fetched when the entity is fetched. FetchType LAZY improves the performance of the application as it reduces the amount of data that needs to be fetched from the database, while FetchType EAGER can lead to poor performance of the application as it can take a long time to fetch the data from the database.
