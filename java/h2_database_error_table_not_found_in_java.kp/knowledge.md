---
title: No table was located in the h2 in-memory database
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The table may not exist in the H2 in-memory database.
---

**Contents**

[TOC]

1. Check Database Setup

Before checking for any issues with the table, it is important to make sure that the database is setup correctly and that the database is connected to the Java application. This includes checking the database connection string, verifying that the database is running, and ensuring that the correct user credentials are being used.

2. Check Table Creation

Once the database setup is verified, it is important to check that the table was actually created. This can be done by using a query tool to connect to the database and running a query to list all of the tables in the database. If the table is not present, then it was likely not created correctly.

3. Check Table Access

If the table is present in the database, then it is important to check that the Java application has access to the table. This can be done by verifying that the correct user credentials are being used and that the user has the correct permissions to access the table.

4. Check Table Name

Finally, it is important to check that the table name is correct. If the table name is incorrect, then the Java application will not be able to find the table. If the table name is correct, then the issue may be related to the database setup or permissions.
