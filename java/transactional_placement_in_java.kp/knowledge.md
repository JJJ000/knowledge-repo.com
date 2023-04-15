---
title: In what location should the @transactional annotation be placed?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The @Transactional annotation belongs on the method or class that needs to be included in the transaction.
---

**Contents**

[TOC]

1. **Overview**
The @Transactional annotation is a Java annotation used to mark a method or class as a transactional resource. It is used to indicate that a method or class should be executed within a transaction context.

2. **Usage**
The @Transactional annotation is usually placed on a class or method. When placed on a class, all of the methods in that class will be executed within a transaction. When placed on a method, only that method will be executed within a transaction.

3. **Benefits**
The @Transactional annotation helps ensure that data is consistent and correct when multiple operations are performed on the same data. It also helps ensure that data is not lost in the event of an error.

4. **Limitations**
The @Transactional annotation is not a replacement for proper database transaction management. It is important to ensure that the underlying database is properly configured to support transactions. Additionally, the @Transactional annotation does not guarantee that a transaction will be committed or rolled back, as the underlying database may not support that functionality.
