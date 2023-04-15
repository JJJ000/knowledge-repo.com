---
title: What are the different options available for the hibernate hbm2ddl.auto property and what do they each accomplish?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The possible values of hbm2ddl.auto are `create`, `create-drop`, `update`, `validate`, `none`, and `auto`; they control how Hibernate generates and updates the database schema when the application is started.
---

**Contents**

[TOC]

### create
When this value is set, Hibernate will create the database schema from the mappings when the SessionFactory is created.

### create-drop
This value will create the schema when the SessionFactory is created, but will drop it when the SessionFactory is closed.

### update
When this value is set, Hibernate will update the database schema whenever the SessionFactory is created. This is the default behavior.

### validate
When this value is set, Hibernate will validate the database schema when the SessionFactory is created. If the schema is out of date, an exception will be thrown.
