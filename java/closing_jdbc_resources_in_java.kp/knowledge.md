---
title: Do jdbc result sets and statements need to be closed individually before the connection is closed?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, JDBC Resultsets and Statements should be closed separately before the Connection is closed.
---

**Contents**

[TOC]

## Yes
When using JDBC, it is important to close all JDBC objects in the correct order. This means that JDBC Statements and Result Sets must be closed before the Connection object is closed.

## Reasons
Closing the Connection object first will close all the Statements and Result Sets associated with it. This may cause errors if the Statements and Result Sets have not been closed already.

Additionally, not closing the Statements and Result Sets can lead to memory leaks and other performance issues. This is because the Statements and Result Sets may still be holding onto resources even after the Connection has been closed.

## Conclusion
Therefore, it is best practice to close JDBC Statements and Result Sets separately from the Connection object in Java. Doing so will help to ensure that all resources are properly released and prevent potential errors and performance issues.
