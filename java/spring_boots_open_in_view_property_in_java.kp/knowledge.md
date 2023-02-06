---
title: What does the spring boot property 'spring.jpa.open-in-view=true' do?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The spring.jpa.open-in-view=true property enables lazy loading of data in Spring Boot applications.
---

**Contents**

[TOC]

## What is Spring Boot? 
Spring Boot is an open source Java-based framework used to create a micro service. It simplifies the development of stand-alone, production-grade Spring based applications. It provides an opinionated approach to configuration and eliminates the need for XML configuration.

## What is the spring.jpa.open-in-view Property?
The spring.jpa.open-in-view property is a configuration property in Spring Boot that enables the use of Open EntityManager In View pattern. This pattern allows JPA entities to be lazily loaded in the view layer. When this property is set to true, the EntityManager will be kept open until the view layer is rendered.

## What are the Benefits of Using Open EntityManager In View?
Using Open EntityManager In View allows for lazy loading of JPA entities in the view layer. This allows for improved performance as the entities are loaded only when they are needed. Additionally, this pattern simplifies the code in the view layer as the entities can be accessed without the need for explicit initialization. 

## What are the Drawbacks of Using Open EntityManager In View?
Using Open EntityManager In View can lead to potential data inconsistency issues if the data is modified outside of the transaction scope. Additionally, it can lead to memory leaks if the EntityManager is kept open for too long. Therefore, it is important to ensure that the EntityManager is closed once the view layer is rendered.
