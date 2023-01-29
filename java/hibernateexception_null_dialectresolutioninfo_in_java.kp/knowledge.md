---
title: An exception occurred in the hibernate library it is not possible to access dialectresolutioninfo when the 'hibernate.dialect' property has not been set
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: If `hibernate.dialect` is not set in Java, an org.hibernate.HibernateException will be thrown, stating that Access to DialectResolutionInfo cannot be null.
---

**Contents**

[TOC]

### Introduction
Hibernate is a popular open source Object-Relational Mapping (ORM) tool used in Java-based applications. It provides a framework for mapping an object-oriented domain model to a relational database. When working with Hibernate, it is important to set the `hibernate.dialect` property in the configuration file. This property is used to determine the database dialect used by Hibernate. If this property is not set, then an exception will be thrown when accessing the DialectResolutionInfo.

### What is the Exception?
The exception thrown when `hibernate.dialect` is not set is: `org.hibernate.HibernateException: Access to DialectResolutionInfo cannot be null when 'hibernate.dialect' not set`. This exception occurs when Hibernate attempts to access the DialectResolutionInfo, but the `hibernate.dialect` property is not set in the configuration file.

### How to Resolve the Exception
The exception can be resolved by setting the `hibernate.dialect` property in the configuration file. This property should be set to the database dialect that is being used. For example, if the database being used is MySQL, then the property should be set to `org.hibernate.dialect.MySQLDialect`.

### Conclusion
It is important to set the `hibernate.dialect` property when working with Hibernate. If this property is not set, then an exception will be thrown when accessing the DialectResolutionInfo. The exception can be resolved by setting the `hibernate.dialect` property in the configuration file.
