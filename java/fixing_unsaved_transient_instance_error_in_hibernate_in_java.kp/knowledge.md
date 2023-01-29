---
title: What steps should be taken to resolve the "object references an unsaved transient instance - save the transient instance before flushing" error in hibernate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Save the transient instance before flushing by calling the Session.save() method.
---

**Contents**

[TOC]

### Understanding the Error
The "object references an unsaved transient instance - save the transient instance before flushing" error is a common issue that occurs when using the Hibernate ORM framework in Java. This error occurs when an entity is referenced in a query or operation before it has been saved to the database.

### Identifying the Source of the Error
The source of the error can usually be identified by looking at the stack trace of the error. The stack trace should provide enough information to determine which entity is causing the issue.

### Resolving the Error
Once the source of the error has been identified, the issue can be resolved by saving the transient instance before performing the query or operation. This can be done by calling the save() or saveOrUpdate() method on the entity before the query or operation is executed.

### Preventing the Error
To prevent this error from occurring in the future, it is important to ensure that all entities are saved to the database before they are used in a query or operation. This can be done by always calling the save() or saveOrUpdate() method on an entity before it is used in a query or operation.
